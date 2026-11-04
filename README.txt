GLOBAL FOCUS HUB — MOBILE WEBSITE PACKAGE
==========================================

FILES
- index.html: responsive website connected to your Supabase project.
- ADMIN_GUIDE.txt: safe manual approval instructions for the first MVP.

IMPORTANT
This is a first connected MVP, not a fully launched production marketplace.
It uses your Supabase Project URL and publishable key in the browser. A publishable
key is intended to be public; never place a secret key, service_role key, or
database password in this file.

WHAT WORKS
- Customer email sign-up and login using Supabase Auth.
- Agent application form saves agency name and phone to the user's profile.
- Published property listings are loaded from the properties table.
- Approved agents can submit property details and upload photos.
- Property submissions start as pending.
- Dashboard shows the user's own submissions.

ADMIN APPROVAL
For this first version, agent and property approvals are performed manually
by the project owner in Supabase SQL Editor. Do not create an admin role in
the public browser or put a service-role key in this website.

DEPLOYMENT
You can use a browser-based static host from your Android phone, but first
test the website locally or on a private preview. When deploying, set the
Supabase Auth Site URL and Redirect URLs to the exact deployed HTTPS domain.
Do not use localhost for the public deployment.

SECURITY / NEXT CHECKS
- Confirm Row Level Security is enabled on profiles and properties.
- The current SQL policies allow public reads only for published properties
  whose agent profile is approved.
- The storage bucket must be named exactly property-images and be public for
  the public image URLs used by this MVP.
- The storage insert policy expects uploads under a folder named with the
  authenticated user's UUID.
- This package does not include payments, maps, messaging, identity-document
  verification, or a fully automated admin panel.
