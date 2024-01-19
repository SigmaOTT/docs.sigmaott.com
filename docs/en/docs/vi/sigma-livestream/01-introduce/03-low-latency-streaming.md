---
title: Low Latency Streaming
order: 3
---

# Low Latency Streaming

## Apple HLS Low Latency

Như đã đề cập ở mục trước. The HTTP Live Streaming (HLS) protocol delivers live and on-demand content streams to global-scale audiences. HLS has historically favored stream reliability over latency. Low-Latency HLS extends the protocol to enable low-latency video streaming while maintaining the same degree of scalability. The new low-latency mode lowers video latencies over public networks into the range of standard television broadcasts.

Backend production tools and content delivery systems must implement new rules to enable low-latency stream playback. Low-latency  to stream HLS (LHLS) segments which have not completed transcoding yet. Segments do not need to be complete to be buffered - each segment contains a number of GOPs (group of pictures), and each GOP can be independently transmuxed and appended to a buffer in the playback user agent. Using HTTP chunked transfer encoding, LHLS is able to maintain a persistent connection with a transcoding server; the server, in turn, is able to push partial segments to the client before completion. Additional reductions in latency are possible by negotiating the TCP connection before the segment needs to be buffered.

A biggest challenge to implement LHLS in production is ABR logic:

1. The available buffer is almost zero by design. This means all minimum buffer sizes for ABR switches and LoadControl configurations become practically useless.
2. The live latency may drift over time because the playback speed (as determined by the renderers) is likely to be not exactly real-time aligned.
3. Rebuffering makes the live latency considerably worse and normal playback speed would never catch up again.Bandwidth estimation based on transfers is only possible if the transfers [happen as fast as possible](https://docs.google.com/document/d/1e3jVkZ6nxNWgCqTNibqV8uJcKo8d597XVl3nJkY7P8c/edit#heading=h.ya5n8kibobz9).
4. This may not be true for partially available media chunks as they only become available in real-time. Moreover, the actual data transfer may be bursty as new small chunks of data are written and then transferred. Similarly, transferring small sub-segment media pieces (in the Apple LHLS case) likely suffers from [estimation inaccuracies caused by small transfer sizes](https://docs.google.com/document/d/1e3jVkZ6nxNWgCqTNibqV8uJcKo8d597XVl3nJkY7P8c/edit#heading=h.omecbu2809cn).
5. Information about other formats may not be available and loading initialization data or new media playlists causes extra initial start-up time for a new format in which the player may already run out of media.

## DASH CMAF Low Latency

Usually when live streaming, the media is sent in segments that are each a few seconds long. These segments shouldn’t be shorter than 2 to 4 seconds or there could be a risk of poor performance/playback quality. With LL-DASH, if the player requests a segment which is not completed, chunks will be delivered as soon as they are available using Chunked Transfer Encoding. As media can be delivered to the client as soon as it is generated on the server side, overhead is reduced, allowing to reduce the client's buffer and, as a result, latency. A client's buffer should contain around 3-4 chunks to guarantee smooth playback, potentially reducing the latency to something of this order of magnitude. In practice, it is also important to take manifest handling, time synchronization and buffering for network issues into account. With LL-DASH, we can reduce the latency to a couple seconds instead of the multiple 10’s of seconds that we had before.
