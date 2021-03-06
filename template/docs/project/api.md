<!-- Generated by documentation.js. Update this documentation by updating the source code. -->

### Table of Contents

-   [ActionBar][1]
    -   [fetchComments][2]
    -   [render][3]
-   [Comment][4]
    -   [updateRating][5]
    -   [comment][6]
    -   [changeRating][7]
    -   [computedClasses][8]
-   [maybeHandleError][9]
-   [fetchComments][10]
-   [Index][11]
    -   [comments][12]
    -   [hasComments][13]
    -   [fetch][14]

## ActionBar

**Extends Vue**

Actions bar component written in jsx.
The main idea of this example is to demostrate flexibility of Vue and jsx.
We discourage using `jsx` in a real world apps,
unless you know what are you doing!

### fetchComments

Typed alias to Vuex `fetchComments` action.

Type: function (): [Promise][15]&lt;[Array][16]&lt;CommentType>>

### render

-   **See: [https://vuejs.org/v2/guide/render-function.html][17]**

Render function. It is an equavalent of `<template>` tag.

Returns **VNode** Virtual node to be rendered by Vue.

## Comment

**Extends Vue**

Comment component is used to represent a single user's comment.

### updateRating

This is a wrapped mutation from the vuex.

Type: function (CommentPayloadType): void

### comment

Passed comment from the parent component.

Type: CommentType

### changeRating

Changes comment's rating.
Can be used to increase or decrease comment's rating.

**Parameters**

-   `commentId` **[number][18]** Comment's identifier to change rating.
-   `delta` **[number][18]** Delta value to change rating value.

### computedClasses

Defines which color borders are.
Uses `comment`'s rating to choose color.

Returns **any** Pairs of class names and boolean values if they should be applied.

## maybeHandleError

Throws error when there is one.

**Parameters**

-   `error` **$AxiosError&lt;T>?** Error instance to be thrown.

Returns **void** 

## fetchComments

Fetches comments from the remote API.

**Parameters**

-   `$axios` **Axios** Slightly modified `Axios` instance from nuxt-axios module.


-   Throws **$AxiosError** If there is one.

Returns **[Promise][15]&lt;[Array][16]&lt;RawCommentType>>** Parsed response data.

## Index

**Extends Vue**

Main page (or index page).
Mounted as `/` by default.

### comments

List of predownloaded comments, bound from Vuex.

Type: [Array][16]&lt;CommentType>

### hasComments

Returns either we have any comments or not.

Type: [boolean][19]

### fetch

-   **See: [https://nuxtjs.org/api/pages-fetch][20]**

Fetches comments from external API from the server side.
This method should preload Vuex store.

**Parameters**

-   `context` **any** Nuxt `context` instance.
    -   `context.store`  Current Vuex store.

Returns **[Promise][15]&lt;[Array][16]&lt;CommentType>>** List of downloaded comments.

[1]: #actionbar

[2]: #fetchcomments

[3]: #render

[4]: #comment

[5]: #updaterating

[6]: #comment-1

[7]: #changerating

[8]: #computedclasses

[9]: #maybehandleerror

[10]: #fetchcomments-1

[11]: #index

[12]: #comments

[13]: #hascomments

[14]: #fetch

[15]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Promise

[16]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array

[17]: https://vuejs.org/v2/guide/render-function.html

[18]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number

[19]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Boolean

[20]: https://nuxtjs.org/api/pages-fetch
