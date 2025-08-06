# Discord Token Guide (PC, iOS & Android)

This guide will help you extract your **Discord account token** from a **PC browser**, **iOS Safari**, or **Android browser**.

---

## 💻 For PC (Windows/macOS – Browser Console Method)

1. Sign into your Discord account at https://discord.com/app  
2. Press `Ctrl + Shift + I` (or `Cmd + Option + I` on Mac) to open **Developer Tools**  
3. Click the **Console** tab  
4. Paste the following script into the console:

```js
webpackChunkdiscord_app.push([[Symbol()],{},r=>{t=Object.values(r.c||{}).find(x=>x?.exports?.getToken)?.exports?.getToken();t&&console.log(t)}]);
```

5. Press **Enter**  

✅ A long string will appear below — this is your **Discord token**.  
Copy it and paste it into the field where needed (e.g. `/redeem credits`).

---

## 📱 For iOS (Safari – Bookmark Method)

> This method is for the **Safari browser on iOS**.

1. Go to the Discord Web App: https://discord.com/app and make sure you're logged in  
2. Tap the **Share** button, then tap **"Add Bookmark"**  
3. (Optional) Rename the bookmark, then tap **Save**  
4. Go to **Bookmarks > Favourites**  
5. Tap **Edit**, then select the bookmark you just created  
6. Delete the pre-filled URL and replace it with this code:

```
javascript:(function()%7Bif(!location.host.includes('discord.com'))%7Balert('You%20need%20to%20click%20the%20bookmark%20on%20Discord.');location.href='https://discord.com/app';return%7Dlocation.reload();var%20i=document.createElement('iframe');document.body.appendChild(i);let%20t=i.contentWindow.localStorage.token;t=t?t.replace(/%5B%22%5D/g,''):null;t?navigator.clipboard.writeText(t).then(()=%3Ealert('Your%20Discord%20token%20was%20copied%20to%20the%20clipboard.')):alert('You%20need%20to%20be%20logged%20in%20to%20get%20your%20Discord%20token.');%7D)()
```

7. Tap **Done**, then go back  
8. Tap the bookmark you just saved  
9. Your Discord token will be copied to your clipboard
---

## 🤖 For Android (Any Mobile Browser – Desktop Site Method)

> This method uses the browser's **desktop site mode** (e.g. Chrome).

1. Open your browser (e.g. Chrome) and go to https://discord.com/app  
2. Tap the browser menu (three dots) and select **"Desktop site"**  
3. Log into your Discord account  
4. Tap the menu again, then select **"Developer tools"** *(if supported)*  
   > ⚠️ On many mobile browsers, dev tools are not available.  
   > Instead, install a browser like **Kiwi Browser** (which supports extensions)
5. Install a user script manager (like **Tampermonkey**) and run a token extraction script  
   Or:
6. Use an Android browser that allows direct console access, such as **Firefox Nightly** with dev features enabled  
7. Once you open the console, paste the same script as the PC method:

```js
webpackChunkdiscord_app.push([[Symbol()],{},r=>{t=Object.values(r.c||{}).find(x=>x?.exports?.getToken)?.exports?.getToken();t&&console.log(t)}]);
```

8. Press **Enter** and copy the token output

✅ That’s your token

## ⚠️ Disclaimer

This guide is for **educational purposes only**.

- **Never share your token** with anyone you do not trust.  
- Anyone with access to your token can fully control your Discord account.  
- You can reset your token at any time by changing your Discord password.  
