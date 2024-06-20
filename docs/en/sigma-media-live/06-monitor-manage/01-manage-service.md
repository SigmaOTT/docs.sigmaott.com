---
title: Service Management
order: 1
---

# {{ $frontmatter.title }}

## Operations with the service

For lists of content, the app allows users to interact with each list element through a group of function buttons (See illustration below).
These buttons will show up in the last column of the list table.

![Action Buttons](/images/media-live/manager-list-action.png)

---

:::info
Because each piece of content on the application has different features and operations, the interface showing the function buttons may differ slightly.
:::

---

### Detailed description

- 'Start': Start the channel.
- 'Stop': Stop the channel
- 'Reset': Stop and restart the channel
- 'Clone' creates a new object with identical data to the original object, while also customizing some parameters of the new object to match.
- 'Delete' deletes the selected object. Before the application performs the deletion, it will ask the user to authenticate again.

## Auto Refresh

![Auto Refresh](/images/media-live/um-auto-refresh.jpg)

Allows automatic data re-updating after a certain period of time on and off.

There are 5 values to choose from: _Off_ and intervals _Time 5s_, _Time 10s_, _Time 15s_, _Time 20s_ corresponding to time values of 5 seconds, 10 seconds, 15 seconds and 20 seconds will automatically update new data for users.

## Filter

In content sections in the form of table lists, there is support for filtering, searching for elements by one or a few specific conditions. Filters are displayed above each table.

After completing the search/filter, valid elements will be displayed on the interface.

### Channel Filter

![Channel Filter](/images/media-live/um-filter/channel.png)

Channel filters allow users to search for data fields such as the following (from left to right on the description figure):

- 'Status' channel status, including 4 options: 'All', 'Live', 'Stopped', 'Error'.

- 'Type' channel type, including 2 options 'Package', 'Transcode'.

  ![Channel Type](/images/media-live/um-filter/type-channel.jpg)

- 'Tag' tag assigned to channel, user enters tag.

- 'Name' identifies the channel, the user enters the channel name to be searched.

## Pagination

![Pagination](/images/media-live/um-pagination/main.png)

Make pagination adjustments to content sections that take the form of a list.

The paging interface consists of 4 main components:

- The total number of existing elements.

  ![Counter Pagination](/images/media-live/um-pagination/counter.png)

- Option the number of elements visible on a page.

  <!-- ![Fontsize Menu](/images/media-live/um-pagination/page-size.png) -->

  ![Page Size](/images/media-live/um-pagination/page-size-selection.jpg)

  The optional '5', '10', '15', '20', '50', '100' elements can be displayed on a page by selecting the corresponding values in the paging menu, the default value is '10'.

- Current page order.

  ![Page Select](/images/media-live/um-pagination/page-selection.png)

  - List existing pages.
  - The current page is highlighted with a blue background color! [Active Page] (/images/media-live/um-pagination/actived-page.png) { height=17px } .
  - Scroll to the previous/next page one by one by selecting the ! [Previous] (/images/media-live/um-pagination/previous.png) { height=17px } and ! [Next] (/images/media-live/um-pagination/next.png) { height=17px } .

- Navigate to any page.

  ![Next](/images/media-live/um-pagination/jump-to.jpg)

  You can move to any page by entering the page number in the box in the image above
