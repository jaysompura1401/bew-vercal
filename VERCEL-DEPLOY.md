# Vercel deploy (frontend)

Backend + MySQL are on Railway: https://backend-production-5f9d8.up.railway.app

1. Push this folder to GitHub (node_modules and .env are git-ignored, do not commit them).
2. vercel.com > Add New > Project > import the repo.
3. Framework Preset: Other. Root Directory: ./  (build command comes from vercel.json).
4. Environment Variables (before first deploy):
   - VITE_API_URL = https://backend-production-5f9d8.up.railway.app/api
   - VITE_GOOGLE_MAPS_API_KEY = <your NEW key, restricted to your Vercel domain>
5. Deploy. Then on Railway > backend > Variables set CLIENT_URL = https://<your-app>.vercel.app (no trailing slash).

Property photos load through the /uploads rewrite in vercel.json (proxied to the Railway backend).
