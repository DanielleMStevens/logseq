---
title: roam/css
---

## 
### ```css
:root{
  --font-size: 15.5 px;
  --border-color: rgba(0, 0, 0, 0.08);
  --subtle-border-color: rgba(0, 0, 0, 0.05);
  --main-background-color: hsl(210, 9%, 98%);
  --body-background-color: #ffffff;
  --reference-item-background: hsl(0, 0%, 99%);
  --brackets-color: rgba(0, 0, 0, 0.25);
  --empty-text-color: hsl(203, 12%, 75%); 
  --page-width: 1000px;
}

/* kalban resizing */
.kanban-board {
  min-width: 1100px;
}
.kanban-column{
  min-width: px;
}
.kanban-card {
  min-width: px;
}


/*table reszing*/
.roam-table {
  min-width: 800px;
}

/*sidebar flexable reszing*/
.roam-center {
   flex-basis: auto !important;
   resize: horizontal !important;
   overflow: auto !important;
}


/*custom tags*/

span.rm-page-ref[data-tag="LabWork"] {background: #f7a62d; color: #fff !important;
    padding: 3px 7px; line-height: 2em; font-weight: 500;
}

span.rm-page-ref[data-tag="IGG Recruitment"] {background: #397fdb; color: #fff !important;
    padding: 3px 7px; line-height: 2em; font-weight: 500;
}

span.rm-page-ref[data-tag="Other"] {background: #ebcc1c; color: #fff !important;
    padding: 3px 7px; line-height: 2em; font-weight: 500;
}

span.rm-page-ref[data-tag="Plant Assay"] {background: #ADCB2A; color: #fff !important;
    padding: 3px 7px; line-height: 2em; font-weight: 500;
}

span.rm-page-ref[data-tag="Dissertation Committee"] {background: #0DBAC6 !important; color: #fff !important;
    padding: 3px 7px; line-height: 2em; font-weight: 500;
}

span.rm-page-ref[data-tag="One-on-One"] {background: #B979CF; color: #fff !important;
    padding: 3px 7px; line-height: 2em; font-weight: 500;
}

span.rm-page-ref[data-tag="Lab Meeting"] {background: #cc3b7a; color: #fff !important;
    padding: 3px 7px; line-height: 2em; font-weight: 500;
}

/* Make page width wider */

.roam-block-container,.roam-block,.rm-block-text {max-width: 1600px;}


.roam-center > div {padding-right: 0px !important;padding-left: 0px !important;}

/* end page widening */

On portrait mode on a cellphone, it’s nice to be able to just scroll horizontally to a full sized right sidebar. Here’s code to do that if interested. cc: @Richard Masters @Murf Pushed this to the theme already! Let me know if this works for you.
/* Mobile horizontally scrollable right sidebar in portrait mode */

@media only screen and (max-width: 600px) {
  .roam-body {
    overflow-x: scroll !important;
    display   : flex;
  }
  .roam-main {
    min-width: 95vw;
  }
  #right-sidebar[style*="flex: 0 0 40%;"] {
    flex: 0 0 95% !important;
  }
  #rm-mobile-bar {
    z-index: 1 !important;
  }
}


.rm-title-untitled,
#block-input-ghost > span,
textarea::placeholder {
  color: var(--empty-text-color) !important; }

body,
div,
textarea,
.level2 {
  font-family: 'Quattro', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif !important; }

iframe {
  border: none !important; }

.loading-astrolabe {
  position: absolute !important;
  width: 80px !important;
  height: 80px !important;
  opacity: 0.3 !important;
  top: calc(50% - 40px) !important;
  left: calc(50% - 40px) !important; }

#roam-sidebar-logo {
  display: none !important; }

body,
#app {
  background: var(--main-background-color) !important; }

.roam-center {
  /* sidebar-to-content-ratio */
  flex-basis: auto !important;
  resize: horizontal !important;
  overflow: auto !important;
  /*flex-basis: 50% !important;*/
  border-left: 1px solid var(--border-color) !important;
  border-top: 1px solid var(--border-color) !important;
  border-right: 1px solid var(--border-color) !important;
  border-radius: 6px;
  box-shadow: 0px 2px 14px rgba(0, 0, 0, 0.04) !important;
  /*overflow: visible !important;*/
  background: var(--body-background-color) !important;
  margin-top: 10px;
  margin-right: 16px;
  margin-left: 16px; }

/*
 .roam-center > div:first-child {
    padding-right: calc(0.5 * (100% - 820px)) !important;
    padding-left: calc(0.5 * (100% - 820px)) !important; }
*/

.roam-topbar {
  background: var(--main-background-color) !important; }
  .roam-topbar input#find-or-create-input {
    box-shadow: none !important;
    border: 1px solid var(--border-color) !important; }

.roam-body,
.roam-topbar,
#right-sidebar,
.roam-sidebar-container {
  background: transparent !important; }

#right-sidebar {
  border: none !important;
  transition: none !important;
  overflow: hidden !important; }
  #right-sidebar h1 {
    font-size: 18px !important; }
  #right-sidebar #roam-right-sidebar-content > div[style] {
    border-bottom: 1px solid var(--subtle-border-color) !important; }
  #right-sidebar .hoverparent,
  #right-sidebar .react-resizable {
    max-width: 100% !important; }
    #right-sidebar .hoverparent img,
    #right-sidebar .react-resizable img {
      max-width: 100% !important; }

.rm-page-ref-tag {
  color: #61baa2 !important; }

span.checkmark {
  top: -2px; }

.rm-level1 div,
.rm-level1 textarea {
  font-size: 22px !important;
  line-height: 1.5 !important; }

.rm-level2 div,
.rm-level2 textarea {
  font-size: 20px !important;
  line-height: 1.5 !important; }

.rm-level3 div,
.rm-level3 textarea {
  font-size: 18px !important;
  line-height: 1.5 !important; }

.level2 {
  font-weight: inherit !important; }

.roam-log-container .roam-log-page {
  border-top: 1px solid var(--subtle-border-color) !important; }
  .roam-log-container .roam-log-page:first-child {
    min-height: 0 !important;
    border-top: none !important; }

.rm-reference-item {
  background: var(--reference-item-background) !important;
  border: 1px solid #f0f0f0 !important;
  border-radius: 6px !important;
  padding: 8px 10px 8px 2px !important; }
  .rm-reference-item .rm-block-text {
    font-size: var(--font-size) !important; }

.CodeMirror {
  font-size: 13px !important; }

.roam-body .roam-app .roam-sidebar-container .roam-sidebar-content .log-button:hover,
.roam-body
.roam-app
.roam-sidebar-container
.roam-sidebar-content
.starred-pages-wrapper
.starred-pages
.page:hover {
  color: inherit !important;
  background-color: transparent !important; }

.roam-body .roam-app .roam-sidebar-container .roam-sidebar-content .log-button,
.roam-body .roam-app .roam-sidebar-container .roam-sidebar-content .starred-pages-wrapper,
.roam-body
.roam-app
.roam-sidebar-container
.roam-sidebar-content
.starred-pages-wrapper
.starred-pages
.page,
.bp3-minimal > div {
  color: #666666 !important;
  font-size: 13px !important; }

.roam-sidebar-content {
  padding: 0 !important; }
  .roam-sidebar-content > div:not(.log-button):not(:first-child) {
    padding: 0 !important; }
  .roam-sidebar-content > div:first-child {
    padding-bottom: 18px !important; }

.starred-pages-wrapper > div:first-child {
  display: none; }
.starred-pages-wrapper .flex-h-box,
.starred-pages-wrapper .flex-h-box span {
  font-size: 13px !important;
  opacity: 0.6 !important; }

.roam-body .roam-app .roam-sidebar-container .roam-sidebar-content .log-button,
.roam-body
.roam-app
.roam-sidebar-container
.roam-sidebar-content
.starred-pages-wrapper
.starred-pages
.page {
  padding: 6px 24px 6px !important; }

.bp3-icon-small {
  padding-left: 24px !important; }

.rm-block-text {
  max-width: 640px !important;
  font-size: var(--font-size) !important; }

.block-bullet-view {
  margin-bottom: 3px !important; }

.roam-article > div > div h1 {
  font-size: 26px !important;
  font-weight: 700 !important;
  height: auto !important;
  line-height: 1.5 !important; }

.rm-title-display,
.rm-title-textarea {
  height: auto !important;
  line-height: 1.5 !important; }

.roam-log-container .roam-log-preview h1 {
  font-size: 22px !important;
  font-weight: 700 !important; }

strong {
  font-weight: 700 !important; }

.block-border-left {
  border-left-color: var(--subtle-border-color) !important; }

.rm-reference-main div > strong {
  color: gray !important; }

@media (prefers-color-scheme: dark) {
  body {
    background: #171717 !important; }

  #app {
    filter: invert(1) hue-rotate(180deg) !important; }

  img,
  div#buffer,
  .bp3-portal,
  .intercom-app,
  .loading-astrolabe,
  .bp3-dialog,
  .twitter-tweet,
  iframe {
    filter: invert(1) hue-rotate(180deg) !important; }

  .roam-highlight {
    background-color: #e2cb47 !important; }

  .bp3-overlay-backdrop {
    background-color: rgba(255, 255, 255, 0.7) !important; }

  :root {
    --border-color: rgba(0, 0, 0, 0.07) !important;
    --subtle-border-color: rgba(0, 0, 0, 0.05) !important;
    --main-background-color: hsl(0, 0%, 96%) !important;
    --body-background-color: hsl(0, 0%, 90%) !important;
    --reference-item-background: hsl(0, 0%, 93%) !important;
    --brackets-color: rgba(0, 0, 0, 0.3) !important;
    --empty-text-color: hsl(203, 5%, 70%); } }


.h1,
.h2,
.h3,
.h4,
.h5,
.h6,
h1,
h2,
h3,
h4,
h5,
h6 {
    font-family: 'Inter';
}

div,
textarea {
  font-family: 'SF Pro Display';
  font-size: 100.7%;
  color: #2d3c4e
}

/*
.roam-block-container {
    max-width: 1000px;
}
*/
.rm-query {
    border: 0.5px solid #e4e9ec;
    border-radius: 5px;
    
}

.rm-query .rm-query-title {
    background-color: #f7f8f8;
    padding: 0.8em;
    color: #d1dbe2;
    font-size: 80%;
}

.rm-reference-main.rm-query-content {
    padding: 0.8em;
}

.rm-reference-main .rm-reference-item .rm-block-text {
    font-size: 90%;
}

.rm-ref-page-view-title span {
    font-size: 115%
}

.rm-reference-main .rm-reference-item .controls {
    margin-left: -1em;
}

.rm-ref-page-view {
    padding: 0.4em 0.2em;
}

.roam-body .roam-app .roam-sidebar-container .roam-sidebar-content .starred-pages-wrapper .starred-pages .page {
    padding: 6px;
    padding-top: 8px;
    font-size: 110%;
}

div.flex-v-box.starred-pages-wrapper > div.flex-h-box > span {
    font-size: 14px;
    opacity: 80%;
    letter-spacing: 0.0em;
}

div.roam-sidebar-container.noselect > div > div {
    font-size: 14px;
    letter-spacing: 0.03em;
    
}

#block-input {
    background: white;
}

.roam-body #block-input > span > div {
    padding: 6px 24px;
    background: white;
}

span.bp3-icon-small.bp3-icon-star {
    display: none;
    visibility: hidden;
}

#right-sidebar > div {
    background-color: #f7f8fa;
}
.rm-page-ref-brackets {
    display: none;
}
.controls .simple-bullet-outer .simple-bullet-inner {
    background-color: #e5e9f2;
}
.block-border-left {
    border-left: 1px solid #fff;
}
.kanban-board {
    background-color: #fff;
}
.kanban-card {
    background-color: white;
    margin: 8px;
    box-shadow: 0px 1px 2px #9EB3C0;
    padding: 10px;
    border-radius: 2px;
    line-height: 1.3em;
}
.kanban-title {
    text-align: center;
    font-weight: bold;
    padding-top: 6px;
}
.kanban-column {
    background-color: #E4EDF2;
    margin: 0px 4px 0px 4px;
    padding: 4px;
    min-width: 200px;
    border-radius: 3px;
}
.rm-block-ref::before {
    content: '';
    display: inline-block;
    width: 10px;
    border-radius: 40px;
    height: 10px;
    background: #33bdea4d;
    margin-right: 5px;
}
.rm-block-ref {
    border-bottom: none;
    font-size: 1em;
    color: #627a9d;
}
.rm-block-ref:hover {
    background: none;
    cursor: pointer;
}
.checkmark {
    background: #fff;
}
.check-container {
    padding-right: 4px;
}
.check-container input:checked ~ .checkmark {
    background: #33bdea;
}
.check-container input:checked ~ .checkmark:after {
    border-color: #fff;
}
.rm-reference-item {
    margin-top: 8px;
    border-radius: 6px;
    border: 1px solid #e4e9ee;
    margin-right: 8px;
    flex: 1 1 100%;
    word-break: break-word;
    background-color: #f7f9fb;
    padding: 8px;
}

.rm-level2 {
    font-size: 1.5em;
}
.rm-level3 {
    color: #939aae;
    font-weight: 400;
    font-size: 1.3em;
}
.rm-page-ref {
    color: #9aabd0;
}
.rm-page-ref-link-color {
    color: #2382A1;
    font-weight: 600;
}
a {
    color: #82AC26;
}
.roam-body .roam-app .roam-sidebar-container {
    background-color: #f7f8fa;
}
.roam-body .roam-app .roam-sidebar-container .roam-sidebar-content .starred-pages-wrapper .starred-pages .page,
.roam-body .roam-app .roam-sidebar-container > * {
    opacity: 80%;
    box-shadow: none;
}
.roam-body .roam-app .roam-sidebar-container .roam-sidebar-content .starred-pages-wrapper .starred-pages .page:hover,
.roam-body .roam-app .roam-sidebar-container .roam-sidebar-content .log-button:hover {
    background: white;
    color: black;
    opacity: 100%;
}
#buffer.tall {
    height: calc(100vh - 50px);
}
.check-container {
    padding-right: 4px;
}
span.rm-page-ref {
    border-radius: 2px;
    padding-left: 1px;
    padding-right: 1px;
}
.content span.rm-page-ref {
    padding: 4px 1px 1px;
    /* required for fixing azo */
}
.center-proj {
    text-align: center;
}

/*
span.rm-page-ref[data-tag="Projects"] {
    background: #7172FC;
    color: #fff;
    padding: 3px 7px;
    line-height: 2em;
    font-weight: 500;
}

span.rm-page-ref[data-tag="Quick Capture"] {
    color: #db3b8d;
    padding: 3px 4px;
    line-height: 1.4em;
    font-weight: 700;
}
*/

/* 
Author: @CatoMinor3
Version: 1.1
Date: June 10th, 2020
PayPal support: https://twitter.com/CatoMinor3/status/1284173182245769216?s=20
How to use it: Write #make:wide etc. in front of an image, pdf or iframe. 
*/


/*Installation: https://twitter.com/amirkhan_____/status/1270511701448781824?s=20 */

[data-tag="make:wide"] ~ div {
	width: 165% !important;
	height: 250% !important;
}


[data-tag="make:wide-on-hover"] ~ div:hover {
  transform: scale(10); 
}

[data-tag*="make:wide"] ~ div div:nth-child(2){
	width: 100% !important;
}



[data-tag="make:long"] ~ div {
	height: 660px !important;
}


[data-tag*="make:long"] ~ div div:nth-child(2){
	height: 100% !important;
}









```
