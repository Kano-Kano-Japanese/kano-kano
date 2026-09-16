# Google Calendar bridge v81 update

1. Open the existing Apps Script project.
2. Replace all contents of `コード.gs` / `Code.gs` with `google-calendar-bridge/Code.gs` from this package.
3. Save (Ctrl+S).
4. Choose **Deploy > Manage deployments**.
5. Edit the existing Web App deployment (pencil icon).
6. Under Version, choose **New version** and deploy.
7. Keep **Execute as: Me** and **Who has access: Anyone**.
8. The `/exec` URL normally stays the same. No change to `BRIDGE_SECRET` is needed.
