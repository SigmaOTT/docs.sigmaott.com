---
title: Glossary
order: 2
---

# Glossary

Here you can learn about terms and concepts that you meet in the documentation on Sigma Media Server.

## Adaptive bitrate streaming

Adaptive bitrate is a method of video streaming over HTTP where the source content is encoded at multiple bitrates.

## Deinterlacing

Deinterlacing is converting an interlaced video to a progressive video.

The interlaced video demonstrates even and odd scan lines as two individual fields. At first, the even lines pass on the screen and then the odd lines pass. Two of such even and odd scan line fields make one video frame. Interlaced videos are great for broadcasting as video images can be processed onto the screen with very little bandwidth. The drawback of interlaced video is that in fast motion, it may be blurred as only half of the image is captured at a time, movement along the frame causes motion artifacts.

Progressive video content shows the even and odd scan lines, that is the entire video frame on the screen at the same time.

Deinterlacing is necessary for comfortable viewing of legacy TV video on PC/mobile devices.

## DVR

This is a set of Sigma features related to recording streams to an archive and then playing the archive via different protocols or exporting the selected part of it to an MP4 file.

## Frame

For video, a frame is one of the many still images which compose the complete moving picture. It is the minimal piece of a video track. Each frame has a start time and a duration.

## Frame duration

For video track, it is the time between the beginning of a frame and the beginning of the next frame.

This parameter is important for some protocols. Normally, frame duration is a difference between timestamps of two neighbouring frames. However, sometimes (when the connection is broken) video breakups are possible. As a result, the delta between two consequent frame timestamps will not be equal to the frame duration. This situation is considered as a frame gap and is handled differently across different protocols.

## GOP (Group of Pictures)

Group of Pictures (GOP) — a structured group of successive frames in an MPEG-encoded video stream. Frames are grouped for the interframe compression purposes. We need compression to transfer video over networks. The encoder software compresses video data to reduce its amount compared with non-compressed (raw) video data.

A compressed stream is a succession of GOPs. On a receiving side, the decoder takes all frames in a GOP and creates an image that you can see.

A GOP consists of an I-frame followed by P-frames and B-frames:

I-frame (keyframe) – is a first frame in a GOP. It is a full image encoded independently from other frames (meaning no links to them). Each GOP has a keyframe at the start.
P-frame, B-frame – frames that go after the keyframe in a GOP.

P-frames contain the difference between the previous P-frame and a current frame. It is encoded with a link to an I-frame.
B-frames contain links to I-frames and P-frames before and after themselves. It helps to rewind quicker, for example.

## GOP size

GOP size (the number of frames between two neighbor keyframes) – the number of frames in one GOP. This number can be variable or constant for a stream. When Sigma transcodes a stream, it creates GOPs of a constant size, so all GOPs have the same size.

## Multicast

Multicast is a method of video distribution in a local network. A multicast is a set of UDP packets transmitted from the same source to a group of subscribers at one time. A special multicast IP address is used.

Learn more in the Sigma documentation

## Prepush

Prepush is a method used to achieve a smoother playback of HTTP MPEG-TS, RTMP, or RTSP video streams transmitted via TCP.

With prepush, a streaming server saves each GOP in the buffer before sending it to a client. When a client connects to the server, the server sends the first GOP from the buffer and then transmits a stream with a timeshift — the delivery lags behind for a time interval equal to the size of one GOP converted to seconds. When the connection with the server breaks or slows down, the client plays a GOP from the buffer. In this way, video is played more evenly.

## Publishing

Publishing is transmitting video to Sigma Media Server from external systems and devices that initiate the connection. Sigma is the party that awaits the connection.

What we call publishing to Sigma:

Transmitting video from a mobile device to Sigma.
Transmitting video from OBS (Open Broadcaster Software) or vMix to Sigma. Learn more
Transmitting video from a webpage to Sigma via WebRTC. Learn more
And this is what we don't call publishing:

Receiving a multicast
Ingesting a stream from some source (in this case it's Sigma that initiates the connection).

## Segments

DASH and HLS protocols break a stream into segments, or chunks. These chunks have a constant duration measured in seconds. Segments are used for transfer and buffering purposes. A segment can contain several GOPs and it must be divisibale by GOP. A segment cannot be shorter than a GOP.

The sender of a DASH or HLS stream transfers video segment by segment, and it sends to a client a so called playlist that is the list of segments. Before the start of playing a stream, the client saves some segments in the buffer. If the connection with the server breaks or slows down, the client plays video segments from the buffer, so video is played more smoothly. The client usually downloads three segments before it strats the playback.

## Transcoder

Transcoder is a component that performs the direct digital-to-digital conversion of the initial video stream to provide a multi-bitrate stream, to change video parameters (codec, image size, bitrate), or to place a logo on top of a video stream.

## Video codecs

It is a technology for compressing raw video for subsequent packaging into a container, which, in turn, will be used for delivery via a specific streaming protocol.

## Video container

A container (or transport) is the format for packaging encoded data in a file or a stream for transmission over a network. Packets with audio and video data are transmitted at the transport layer according to the OSI model.

The container format is self-sufficient and independent of the delivery protocol, that is, you can package the data and play them on your local machine, and not necessarily transfer them over the network.

## Video streaming protocol

Video streaming protocol is the rules for the exchange of data, commands and responses to them between two participants in a video communication (client-server or peer-to-peer).

When preparing data for transmission over the network:

First, the video and audio data must be compressed
Then they must be packed in a container for streaming via a certain protocol.
