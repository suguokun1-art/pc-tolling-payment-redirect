# PC Tolling Payment Redirect

This static site is the stable QR entry for the payment demo.

The QR should point to the deployed site URL. The site reads `current-payment-url.json` and redirects the phone browser to the current Cloudflare quick tunnel payment page.

Update the current target after starting the PC backend and quick tunnel:

```powershell
powershell -ExecutionPolicy Bypass -File ..\scripts\update_payment_redirect_site.ps1
```
