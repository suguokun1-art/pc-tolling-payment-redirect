# PC Tolling Payment Redirect

Repository: `pc-tolling-payment-redirect`

This static site is the stable QR entry for the payment demo.

The QR should point to the deployed site URL. The site reads `current-payment-url.json` and redirects the phone browser to the current Cloudflare quick tunnel payment page.

This site does not process payment data. The real payment page and API still run on the PC backend through the current quick tunnel.

Update the current target after starting the PC backend and quick tunnel:

```powershell
powershell -ExecutionPolicy Bypass -File ..\scripts\update_payment_redirect_site.ps1
```

After the site has a public static URL, generate the serial-screen QR:

```powershell
powershell -ExecutionPolicy Bypass -File ..\scripts\update_payment_redirect_site.ps1 -StableRedirectUrl "https://your-public-static-url/"
```
