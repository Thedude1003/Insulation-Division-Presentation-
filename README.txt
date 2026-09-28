PERMA-SEAL HOME ENERGY VISIT - iPad setup

FOR IT / WEB TEAM
1. Upload this whole "home-visit" folder to an HTTPS web server, for example
   https://www.permaseal.net/home-visit/  (HTTPS is required for offline mode).
2. Serve manifest.webmanifest as application/manifest+json (most servers already do).
3. Open https://<your-site>/home-visit/ once in Safari to confirm it loads.
4. Managed iPads (Jamf, Intune, etc.): push the URL as a Web Clip with
   "Full Screen" on, label "Home Visit", icon icon-180.png.

FOR EACH REP (unmanaged iPads)
1. Open the link in Safari while on Wi-Fi.
2. Tap Share > Add to Home Screen > Add.
3. Open "Home Visit" from the home screen once while online. After that it opens offline.

UPDATING
1. Replace index.html on the server.
2. In sw.js, change VERSION (home-visit-v1 -> home-visit-v2) and upload it.
3. Reps get the update the next time they open the app on Wi-Fi.

NOTES
- Appointment entries are stored only on that iPad and are cleared by "New appointment".
  Nothing is sent to Salesforce or any server.
- Deleting the home-screen app or clearing Safari website data erases the offline copy
  and any unsaved appointment.
