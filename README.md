# Rise Again Initiative
Responsive NGO website and Supabase-backed staff portal for Rise Again Initiative, Kampala, Uganda.

## Included
Public website with mission, programmes, recovery pathway, 18 support-group categories, donation pledges, volunteer applications, sponsor/partner areas, resources, FAQ and contact. Includes responsive styling, original phoenix SVG identity, Supabase-connected forms, authenticated staff portal, database schema for programmes, partners, events, outreach, volunteers, enquiries, donation intents, donations, expenses, beneficiaries, restricted case notes and audit records, and GitHub Pages deployment workflow.

## GitHub Pages
In repository Settings → Pages select GitHub Actions as deployment source. Push to main; the workflow publishes to https://jrsninja.github.io/rise-again-initiative/ after a successful run.

## Activate Supabase
1. Create a Supabase project.
2. Run supabase/migrations/001_initial_schema.sql in SQL Editor.
3. Add project URL and anon/public key to config.js. Never use the service-role key in frontend code.
4. Create staff users in Supabase Auth and add their profile row. Set the first trusted user role to admin.
5. Set verified public email and phone in config.js.
6. Test submissions and RLS with test accounts before launch.

## Donations
The donation form records a donation intention; it does not collect money or claim payment completion. Real payments require an approved merchant account, server-side checkout creation, verified webhooks, reconciliation and receipts. Keep payment secrets server-side.

## Privacy and safeguarding
Do not collect beneficiary case details through public forms. Case-management tables are schema foundations only; the supplied staff policies are broad and must be tightened by role before real sensitive casework. Enable MFA, least-privilege access, retention/deletion rules, backups and incident response. Have local legal/privacy and safeguarding professionals review policies before launch.

Replace unconfirmed contact details and verify NGO registration, governance, programme availability, referral partners, office hours and authorised donation channels before public promotion. No impact statistics or clinical services are claimed.