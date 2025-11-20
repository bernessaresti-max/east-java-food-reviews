<!--
Repository: east-java-food-reviews
Starter: Single-page web app using Firebase (Authentication + Firestore)
Files included below. Follow README for setup and deployment to GitHub + GitHub Pages.
-->

===== FILE: README.md =====
# East Java Culinary Reviews — Starter

A minimal, open, public review web app for culinary places in East Java. Anyone can view reviews, sign in, and post their own reviews (similar to Google Reviews). This starter uses Firebase (Authentication + Firestore) so you don't need to build a backend.

## Features
- Public list of reviews for places in Jawa Timur
- Users can sign in (Google / Email) and leave reviews
- View all reviews by a user
- Simple search / filter by city or keyword
- Deployable to GitHub Pages or Firebase Hosting

## Files in this starter
- `index.html` — single-page frontend (uses Firebase v9 modular SDK)
- `styles.css` — basic styling
- `app.js` — main JS for UI & Firebase logic
- `firebase.rules` — example Firestore rules

## Setup (quick)
1. Create a Firebase project at https://console.firebase.google.com
2. Enable **Authentication**: Google Sign-in and Email/Password (optional)
3. Create a **Firestore** database (production rules shown below)
4. Copy Firebase config and paste into `index.html` (`firebaseConfig` placeholder)
5. Option A: Deploy to GitHub Pages. Push repo, enable Pages from `main` branch `/ (root)`.
   Option B: Deploy to Firebase Hosting: `firebase init hosting` then `firebase deploy`.

## Firestore structure (recommended)
- `reviews` (collection)
  - `{reviewId}` document fields:
    - `placeName` (string)
    - `city` (string)
    - `rating` (number, 1-5)
    - `text` (string)
    - `userId` (string)
    - `displayName` (string)
    - `createdAt` (timestamp)
- `users` (collection)
  - `{userId}`
    - `displayName`, `photoURL`, `joinedAt`

## Security rules (very basic - adapt before production)
See `firebase.rules` in this repo.

## Notes
- This is a starter: you can extend with images, place pages, moderation, likes, search indexing.

-----

===== FILE: firebase.rules =====
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {

    // public read for reviews
    match /reviews/{reviewId} {
      allow read: if true;
      // create if authenticated
      allow create: if request.auth != null &&
        request.resource.data.userId == request.auth.uid &&
        request.resource.data.rating is number &&
        request.resource.data.rating >= 1 && request.resource.data.rating <= 5;
      // allow update/delete only by owner
      allow update, delete: if request.auth != null && request.auth.uid == resource.data.userId;
    }

    match /users/{userId} {
      allow read: if true;
      allow create: if request.auth != null && request.auth.uid == userId;
      allow update: if request.auth != null && request.auth.uid == userId;
    }
  }
}

-----

===== FILE: index.html =====
<!doctype html>
<html lang="id">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width,initial-scale=1">
  <title>Ulasan Kuliner Jawa Timur</title>
  <link rel="stylesheet" href="styles.css">
  <!-- Firebase SDK (v9 modular) -->
  <script type="module" src="https://www.gstatic.com/firebasejs/9.23.0/firebase-app-compat.js"></script>
  <script type="module" src="https://www.gstatic.com/firebasejs/9.23.0/firebase-auth-compat.js"></script>
  <script type="module" src="https://www.gstatic.com/firebasejs/9.23.0/firebase-firestore-compat.js"></script>
</head>
<body>
  <header>
    <h1>Ulasan Kuliner — Jawa Timur</h1>
    <div id="auth-area">
      <button id="btn-signin">Masuk</button>
      <button id="btn-signout" hidden>Keluar</button>
    </div>
  </header>

  <main>
    <section id="controls">
      <input id="search" placeholder="Cari nama tempat atau kata kunci...">
      <select id="city-filter">
        <option value="">Semua kota</option>
        <option value="Surabaya">Surabaya</option>
        <option value="Malang">Malang</option>
        <option value="Kediri">Kediri</option>
        <option value="Jember">Jember</option>
        <!-- tambahkan sesuai kebutuhan -->
      </select>
      <button id="btn-new-review">Tulis Ulasan</button>
    </section>

    <section id="reviews-list">
      <!-- list of reviews will be injected here -->
    </section>
  </main>

  <!-- simple modal for new review -->
  <div id="modal" class="hidden">
    <form id="form-review">
      <h2>Tulis Ulasan</h2>
      <label>Nama Tempat<input name="placeName" required></label>
      <label>Kota<input name="city" required></label>
      <label>Rating
        <select name="rating">
          <option value="5">5</option>
          <option value="4">4</option>
          <option value="3">3</option>
          <option value="2">2</option>
          <option value="1">1</option>
        </select>
      </label>
      <label>Ulasan<textarea name="text" rows="4" required></textarea></label>
      <div class="actions">
        <button type="submit">Kirim</button>
        <button type="button" id="btn-cancel">Batal</button>
      </div>
    </form>
  </div>

  <script>
  // --- IMPORTANT: Replace this firebaseConfig object with your project's config ---
  const firebaseConfig = {
    apiKey: "REPLACE_ME",
    authDomain: "REPLACE_ME",
    projectId: "REPLACE_ME",
    // ... rest of config
  };
  </script>
  <script type="module" src="app.js"></script>
</body>
</html>

-----

===== FILE: styles.css =====
/* Modern Gen-Z inspired UI — soft gradients, rounded corners, smooth shadows */
:root{
  --bg:#f5f7fb;
  --card:#ffffff;
  --primary:#6c5ce7;
  --primary2:#a29bfe;
  --text:#1b1b1b;
  --radius:16px;
  --shadow:0 6px 20px rgba(0,0,0,0.08);
}
body{
  font-family:'Inter',system-ui,-apple-system,Roboto,Arial;
  margin:0;
  background:var(--bg);
  color:var(--text);
}
header{
  display:flex;justify-content:space-between;align-items:center;
  padding:1rem 1.4rem;
  background:linear-gradient(135deg,var(--primary),var(--primary2));
  color:white;
  box-shadow:var(--shadow);
}
h1{font-size:1.6rem;margin:0;font-weight:700;}
#auth-area button{
  background:white;color:var(--primary);
  border:none;padding:.5rem 1rem;
  border-radius:var(--radius);
  cursor:pointer;font-weight:600;
}
#controls{
  display:flex;gap:.6rem;padding:1rem;
  background:#fff;
  position:sticky;top:0;z-index:10;
  box-shadow:var(--shadow);
}
#controls input, #controls select{
  padding:.6rem .8rem;
  border-radius:var(--radius);
  border:1px solid #ddd;
  width:180px;
  font-size:.9rem;
}
#btn-new-review{
  background:var(--primary);
  color:white;border:none;padding:.6rem 1rem;
  border-radius:var(--radius);
  font-weight:600;cursor:pointer;
}
#reviews-list{
  padding:1rem;
  display:grid;gap:1rem;
}
.review{
  background:var(--card);
  padding:1.2rem;
  border-radius:var(--radius);
  box-shadow:var(--shadow);
  transition:.3s;
}
.review:hover{transform:translateY(-3px);} 
#modal{position:fixed;inset:0;background:rgba(0,0,0,0.4);display:flex;align-items:center;justify-content:center}
#form-review{
  background:#fff;
  padding:1.4rem;
  border-radius:var(--radius);
  width:350px;
  box-shadow:var(--shadow);
}
#form-review input,#form-review textarea,#form-review select{
  width:100%;padding:.5rem;margin:.4rem 0 1rem;
  border-radius:var(--radius);
  border:1px solid #ddd;
}
#form-review button{
  padding:.6rem 1rem;border:none;border-radius:var(--radius);
  cursor:pointer;font-weight:600;
}
#form-review button[type="submit"]{background:var(--primary);color:#fff;}
#btn-cancel{background:#ddd;}
-----

===== FILE: app.js =====
// Single-file minimal Firebase app (compat imports used in index.html)
// This file expects firebaseConfig to be available on window

import { initializeApp } from 'https://www.gstatic.com/firebasejs/9.23.0/firebase-app-compat.js';
import { getAuth, GoogleAuthProvider, signInWithPopup, signOut, onAuthStateChanged } from 'https://www.gstatic.com/firebasejs/9.23.0/firebase-auth-compat.js';
import { getFirestore, collection, addDoc, query, orderBy, limit, onSnapshot, where, serverTimestamp, getDocs } from 'https://www.gstatic.com/firebasejs/9.23.0/firebase-firestore-compat.js';

const app = initializeApp(firebaseConfig);
const auth = getAuth(app);
const db = getFirestore(app);

// UI refs
const btnSignIn = document.getElementById('btn-signin');
const btnSignOut = document.getElementById('btn-signout');
const btnNew = document.getElementById('btn-new-review');
const modal = document.getElementById('modal');
const form = document.getElementById('form-review');
const reviewsList = document.getElementById('reviews-list');
const searchInput = document.getElementById('search');
const cityFilter = document.getElementById('city-filter');
const btnCancel = document.getElementById('btn-cancel');

btnSignIn.addEventListener('click', async ()=>{
  const provider = new GoogleAuthProvider();
  try{
    await signInWithPopup(auth, provider);
  }catch(e){alert('Gagal login: '+e.message)}
});
btnSignOut.addEventListener('click', ()=>signOut(auth));

onAuthStateChanged(auth, user=>{
  if(user){
    btnSignIn.hidden = true; btnSignOut.hidden = false;
  }else{
    btnSignIn.hidden = false; btnSignOut.hidden = true;
  }
});

btnNew.addEventListener('click', ()=>{
  if(!auth.currentUser){
    alert('Silakan masuk dulu untuk menulis ulasan.');
    return;
  }
  modal.classList.remove('hidden');
});

btnCancel.addEventListener('click', ()=> modal.classList.add('hidden'));

form.addEventListener('submit', async (e)=>{
  e.preventDefault();
  const fd = new FormData(form);
  const placeName = fd.get('placeName').trim();
  const city = fd.get('city').trim();
  const rating = Number(fd.get('rating'));
  const text = fd.get('text').trim();
  if(!placeName || !text) return alert('Lengkapi semua field');
  try{
    await addDoc(collection(db,'reviews'),{
      placeName, city, rating, text,
      userId: auth.currentUser.uid,
      displayName: auth.currentUser.displayName || 'Anon',
      createdAt: serverTimestamp()
    });
    form.reset();
    modal.classList.add('hidden');
    alert('Ulasan dikirim');
  }catch(err){console.error(err);alert('Gagal kirim ulasan')}
});

// Real-time listener with basic filter
let unsubscribe = null;

function startListener(){
  if(unsubscribe) unsubscribe();
  let q = query(collection(db,'reviews'), orderBy('createdAt','desc'));
  // local filtering will be applied too
  unsubscribe = onSnapshot(q, snap=>{
    const all = [];
    snap.forEach(d=>{
      const data = d.data();
      data.id = d.id;
      all.push(data);
    });
    renderList(all);
  });
}

function renderList(all){
  const search = searchInput.value.toLowerCase();
  const city = cityFilter.value;
  const filtered = all.filter(r=>{
    if(city && r.city !== city) return false;
    if(!search) return true;
    return (r.placeName && r.placeName.toLowerCase().includes(search)) || (r.text && r.text.toLowerCase().includes(search));
  });
  reviewsList.innerHTML = '';
  if(filtered.length===0) reviewsList.innerHTML = '<p>Tidak ada ulasan.</p>';
  filtered.forEach(r=>{
    const el = document.createElement('div'); el.className='review';
    el.innerHTML = `<strong>${escapeHtml(r.placeName || '')}</strong>
      <div>Rating: ${r.rating || '-'} — ${r.city || ''}</div>
      <p>${escapeHtml(r.text || '')}</p>
      <small>oleh <a href="#" data-user="${r.userId}">${escapeHtml(r.displayName||'Anon')}</a></small>`;
    const userLink = el.querySelector('a[data-user]');
    userLink.addEventListener('click', (e)=>{
      e.preventDefault();
      viewUserReviews(r.userId, r.displayName);
    });
    reviewsList.appendChild(el);
  });
}

async function viewUserReviews(userId, displayName){
  const q = query(collection(db,'reviews'), where('userId','==',userId), orderBy('createdAt','desc'));
  const snap = await getDocs(q);
  const arr = [];
  snap.forEach(d=>arr.push(d.data()));
  // simple popup
  alert(`Ulasan oleh ${displayName}:\n\n` + arr.map(a=>`${a.placeName} (${a.city}) — ${a.rating}\n${a.text}\n`).join('\n---\n'));
}

searchInput.addEventListener('input', ()=>{/* local render updates handled by listener's data */});
cityFilter.addEventListener('change', ()=>{});

function escapeHtml(s){ return String(s).replace(/[&<>"']/g, c=>({"&":"&amp;","<":"&lt;",">":"&gt;","\"":"&quot;","'":"&#39;"}[c])); }

startListener();

// optional: expose for debugging
window._fj = {startListener};

-----

<!-- End of files -->
