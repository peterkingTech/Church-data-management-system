The AMEN TECH — Church Management App
The AMEN TECH is a modern, full-featured Church Management System (ChMS) designed to empower churches with seamless administration, communication, and community growth tools. Built with React, Supabase, TailwindCSS, and TypeScript, it supports secure multi-role access, multilingual support, and persistent cloud storage.

🚀 Features
✅ User Authentication (Supabase Auth)

📷 Profile Image Upload via Supabase Storage

🙋 Role-Based Access Control (Admin, Pastor, Member, etc.)

🗂️ Member Registration & Management

🏛️ Department & Groups Management

📅 Event & Service Scheduling

💬 Announcements and Notifications

🌍 Multi-language Support

🔒 Row-Level Security (RLS) with Supabase

📦 Cloud-hosted and Scalable

🛠️ Tech Stack
Layer	Tech
Frontend	React + TypeScript
Styling	TailwindCSS
Backend-as-a-Service	Supabase (DB, Auth, Storage, RLS)
Hosting	(Your host e.g., Vercel / Netlify)

🧑‍💻 Getting Started
1. Clone the repository
bash
Copy
Edit
git clone https::https://github.com/peterkingTech/Church-data-management-system
cd amen-tech
2. Install dependencies
bash
Copy
Edit
npm install
3. Setup Supabase
Create a Supabase project: https://app.supabase.com

Copy your Project URL and Anon Key

Create a .env.local file in the root and add:

env
Copy
Edit
VITE_SUPABASE_URL=your-supabase-url
VITE_SUPABASE_ANON_KEY=your-anon-key
4. Run the app
bash
Copy
Edit
npm run dev
🧩 Supabase Setup
Make sure your Supabase has:

A users table with columns:

id, email, full_name, role, avatar_url

A bucket named avatars in Supabase Storage

RLS policies allowing:

insert and update for authenticated users on their own profile

upload and read on avatars for authenticated users

📁 Project Structure
bash
Copy
Edit
src/
│
├── components/       # Reusable UI components
├── context/          # Auth & global contexts
├── pages/            # Page-level components
├── types/            # Shared TypeScript types
├── utils/            # Helper functions
├── supabase.ts       # Supabase client setup
└── App.tsx           # Main app entry
🧪 Coming Soon
📊 Analytics Dashboard

🧾 Offering & Financial Tracking

🕊️ Prayer Requests

✉️ Email & SMS Communication Tools

📱 Mobile Version (PWA)

🙏 Contributing
Want to contribute? Feel free to fork the repo and submit a pull request! All help to improve this platform for Kingdom work is welcome.

📜 License
This project is open-source under the MIT License.

💡 Inspiration
“Let all things be done decently and in order.”
— 1 Corinthians 14:40

