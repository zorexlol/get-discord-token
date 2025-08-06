# Discord Token Guide

This guide will walk you through how to safely extract your **Discord account token** from your browser console. This is required for use in automated Nitro claim systems or similar bots.

---

## ⚙️ Steps

### 1. Sign into your Discord account
Make sure you're logged into the account you want to extract the token from.

### 2. Open the developer console  
Press `Ctrl + Shift + I` (or `Cmd + Option + I` on Mac) to open the Developer Tools.

- Then click on the **Console** tab at the top.

### 3. Paste the script  
In the Console, paste the following script:

```js
webpackChunkdiscord_app.push([[Symbol()],{},r=>{t=Object.values(r.c||{}).find(x=>x?.exports?.getToken)?.exports?.getToken();t&&console.log(t)}]);
