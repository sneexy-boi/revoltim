# revolt im

a shrimple theme for [Revolt](https://revolt.chat) that replicates somewhat of a traditional messaging application (specifically - this copies the [Signal](https://signal.org) desktop application style)

use this theme override to import the correct colors and (hopefully latest and up to date) custom css:

```
{"accent":"#FD6671","background":"#191919","foreground":"#F6F6F6","block":"#2D2D2D","message-box":"#363636","mention":"rgba(251, 255, 0, 0.06)","success":"#65E572","warning":"#FAA352","tooltip":"#000000","error":"#ED4245","hover":"rgba(0, 0, 0, 0.1)","scrollbar-thumb":"#848484","scrollbar-track":"transparent","primary-background":"#121212","primary-header":"#4a4a4a","secondary-background":"#2e2e2e","secondary-foreground":"#C8C8C8","secondary-header":"#4a4a4a","tertiary-background":"#3b3b3b","tertiary-foreground":"#848484","status-online":"#3ABF7E","status-away":"#F39F00","status-focus":"#4799F0","status-busy":"#F84848","status-streaming":"#977EFF","status-invisible":"#A5A5A5","light":false,"css":":root {\n  --chat-bg: var(--primary-background);\n  --message-box-padding: 8px 8px 8px 0;\n}\n\n/* adds borders after server list and channel list */\n[class^=\"Base-sc-\"]>.list,\n[class^=\"ServerSidebar__ServerBase-sc-\"] {\n  border-right: 1px solid var(--primary-header);\n  background: var(--secondary-background);\n}\n\n/* replacement server swoosh ~ not working currently */\n[class^=\"SwooshWrapper-sc-\"]>svg>path:nth-child(2),\n[class^=\"SwooshWrapper-sc-\"]>svg>path:nth-child(3),\n[class^=\"SwooshWrapper-sc-\"]>svg>rect {\n  display: none;\n}\n\n[class^=\"SwooshWrapper-sc-\"]>svg>path:first-child {\n  fill: var(--primary-header);\n  transform: translateX(.8px) scale(.9);\n  transform-origin: center;\n}\n\n/* unround the channels list */\n[class^=\"ServerSidebar__ServerBase-sc-\"] {\n  border-radius: 0px;\n}\n\n/* remove the settings icon in the server list (unneeded imo and also allows a nicer removal of the shadow) */\n[class^=\"Base-sc-\"]>[class^=\"ItemContainer-sc-\"],\n[class^=\"Base-sc-\"]>[class^=\"Shadow-sc-\"] {\n  display: none;\n}\n\n/* solid header */\n[class^=\"Header-sc-\"] {\n  background: var(--primary-header);\n}\n\n/* smaller chat avatar */\n[class^=\"MessageBase__MessageInfo-sc-\"]>[class^=\"IconBase-sc-\"] {\n  width: 24px;\n  height: 24px;\n}\n\n/* smaller padding above/below messages */\n[class^=\"MessageBase-sc-\"] {\n  padding: 0.05rem;\n}\n\n/* smaller username */\n.detail>[class^=\"UserShort__Name-sc-\"] {\n  font-size: 11px;\n}\n\n/* smaller date */\n[class^=\"MessageBase__DetailBase-sc-\"] {\n  font-size: 9px;\n}\n\n/* moves the message slightly to the left for the smaller chat avatar */\n[class^=\"MessageBase__MessageInfo-sc-\"] {\n  margin-right: -10px;\n}\n\n/* rounded reactions */\n[class^=\"sc-jSgvzq\"] {\n  border-radius: 50px;\n}\n\n/* message bubble */\n[class^=\"MessageBase__MessageContent-sc-\"] {\n  background-color: var(--message-box);\n  border-radius: 18px;\n  padding: 10px 13px 10px 13px;\n  flex-grow: 0;\n}\n\n[class^=\"RevoltApp__Routes-sc-\"] {\n  background: var(--chat-bg);\n}\n\n/* move the message options slightly up a little to not obscure the message */\n[class^=\"sc-iBPTik\"] {\n  top: -27px;\n}\n\n/* transparent bottom box */\n[class^=\"MessageBox__Base-sc-\"] {\n  background: transparent;\n  padding-bottom: 7px;\n}\n\n/* redo margins because message box was kinda off */\n[class^=\"MessageBox__FileAction-sc-\"],\n[class^=\"MessageBox__Action-sc-\"] {\n  margin-bottom: -7px;\n}\n\n/* typing indicator */\n[class^=\"TypingIndicator__Base-sc-\"]>div {\n  background: transparent;\n  backdrop-filter: none;\n}\n\n[class^=\"TypingIndicator__Base-sc-\"]>div>.avatars {\n  margin-left: 13px;\n}\n\n[class^=\"TypingIndicator__Base-sc-\"]>div>.usernames {\n  margin-left: 6px;\n  padding-left: 5px;\n  padding-right: 5px;\n  background: var(--message-box);\n  border-radius: 8px;\n}\n\n/* reply notice */\n[class^=\"ReplyBar__Base-sc-\"] {\n  padding: 0px 10px;\n  margin-left: 52px;\n  margin-right: 58px;\n  border-radius: 16px;\n}\n\n/* modified file upload preview/emoji selection */\n[class^=\"AutoComplete__Base-sc-\"] {\n  margin-left: 52px;\n  margin-right: 58px;\n}\n\n[class^=\"AutoComplete__Base-sc-\"]>div,\n[class^=\"AutoComplete__Base-sc-\"]>div>button {\n  border-radius: 18px;\n}\n\n[class^=\"FilePreview__Container-sc-\"] {\n  margin-left: 52px;\n  margin-right: 58px;\n  border-radius: 18px;\n}\n\n/* signal-like messagebar */\ntextarea#message {\n  background: var(--message-box);\n  border-radius: 18px;\n  margin-left: -10px;\n  padding-left: 10px;\n  margin-top: 5px;\n}\n\n/* recolors the members bar to merge in better with the chat backgorund */\n[class^=\"MemberList__ListCategory-sc-\"],\n[class^=\"SidebarBase__GenericSidebarBase-sc-\"] {\n  background: var(--primary-background);\n}","font":"Lexend","monospaceFont":"JetBrains Mono"}
```

> possible names for this project: signolt

# screenshot

wip

# Options

## Gradients

To apply gradients, you have to change the following value from the top of the CSS:

```
:root {
  --chat-bg: var(--primary-background);
}  
```

Replace `var(--primary-background)` with one of the following gradients:
```
linear-gradient(to top, #eb3349, #f45c43)
```

