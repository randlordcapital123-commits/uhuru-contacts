UHURU DIGITAL SOLUTION CONTACT BASE - SUPABASE VERSION

CONTACT FIELDS
1. Automatic Number (starts at 1)
2. Business Name
3. Business Address / Place
4. Contact Number / WhatsApp

SINGLE SAVE
Enter Business Name, Address / Place and Contact Number, then click SAVE CONTACT.

BULK SAVE
1. Enter ONE Business Name.
2. Enter ONE Address / Place.
3. Paste many different phone numbers, one per line.
4. Click SAVE BULK NUMBERS.

Every saved contact receives its own automatic number: 1, 2, 3, etc.
If a contact is deleted, the remaining contacts are renumbered to keep the list sequential.

DATA
Contacts are stored in your Supabase project (cloud Postgres database), not in the browser.
See SUPABASE SETUP below to connect it. Backup JSON and Restore JSON still work as before.

SUPABASE SETUP
1. Create a project at supabase.com (you're already logged in with GitHub).
2. Open the SQL Editor in your project and run supabase_setup.sql (included in this zip).
3. Go to Project Settings > API and copy your Project URL and anon public key.
4. Open app.js and paste them into SUPABASE_URL and SUPABASE_ANON_KEY at the top of the file.
5. Re-open index.html (or re-upload the files to your host) - the app now reads/writes to Supabase.

SECURITY NOTE
This app has no login screen, so the SQL policy allows anyone with your anon key
(visible in your site's source code) to read/write the contacts table. Fine for
personal/internal use; add Supabase Auth later if you need per-user access control.
