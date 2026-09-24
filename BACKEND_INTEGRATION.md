# পাঠচত্ত্বর — Frontend Handoff

এই package-এ পাঠচত্ত্বরের approved frontend prototype রাখা হয়েছে। `index.html` বর্তমানে standalone HTML হিসেবে কাজ করে এবং embedded assets ব্যবহার করে।

## Backend integration plan

### Firebase services
- Firebase Authentication — Editor login
- Cloud Firestore — reading sessions, books, borrow records, e-books, memories, users
- Firebase Storage — memory photos and permitted e-book PDFs
- Firebase Hosting — production hosting/custom domain
- Firebase Security Rules — public read vs editor-only write permissions

### Suggested Firestore collections
- `users`
- `reading_sessions`
- `books`
- `borrow_records`
- `ebooks`
- `memories`

### Frontend sections / anchors
- `#top` — Home / hero
- `#next` — আগামী পাঠচক্র
- `#books` — বইঘর
- `#memories` — স্মৃতি / recent memories
- `#ebooks` — ই-বুক categories
- `#join` — যুক্ত হোন
- `#all-books` — all books page/view
- `#ebook-bangla` — বাংলা সাহিত্য
- `#ebook-english` — ইংরেজি সাহিত্য
- `#ebook-science` — বিজ্ঞান ও শিক্ষামূলক
- `#ebook-history` — ইতিহাস, সমাজ ও জ্ঞান
- `#archive` — স্মৃতি archive

## Editor login
The current frontend contains a prototype/demo editor-login flow only. Replace the demo authentication with Firebase Authentication before production. Do not keep demo credentials in production source code.

## Privacy
Borrow records containing member names should be editor-only. Public visitors should see book availability and, if desired, due-date information without exposing members' personal names.

## E-books
Only public-domain or otherwise legally distributable PDFs should be uploaded for public download/read access.

## Deployment
`index.html` can be used as the initial Firebase Hosting entry point. Firebase SDK/config and backend code should be added during the backend integration stage.
