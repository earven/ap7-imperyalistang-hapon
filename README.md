# AP7 Quest: Ang Imperyalistang Hapon
> **Interaktibong Modyul sa Pag-aaral at Ranggo (Grade 7 - Araling Panlipunan)**

Isang gamified web application para sa pag-aaral ng Kasaysayan ng Imperyalistang Hapon sa Silangan at Timog-Silangang Asya (mula Panahong Sakoku, Meiji Restoration, Greater East Asia Co-Prosperity Sphere, hanggang sa Ikalawang Digmaang Pandaigdig at Okupasyon sa Pilipinas).

---

## 🎮 Mga Tampok (Features)
- **Role & Character Selection**: Pagpili ng Avatar (Mandirigma, Iskolar, Manlalakbay, Bayani), Pangalan, Seksyon, at 4-Digit PIN.
- **Level & XP Gamification**: Nakakakuha ng XP sa pagbabasa ng aralin, pag-check sa mahahalagang tala, at pagsagot sa flashcards.
- **Audio Feedback**: Built-in sound effects gamit ang Tone.js (synthesized audio nang walang external MP3 files).
- **Boss Battle / Quiz Portal**: 12-item timed review quiz na may Buhay (Hearts), Combos, at Power-ups (50/50, Hint, Time Freeze).
- **Top Leaderboard (Ranggo)**: Podium display para sa Top 1, Top 2, at Top 3 na may full ranking table.
- **Teacher Admin Mode**: Naka-PIN protect na Visual & JSON Editor upang makapagdagdag o makapag-edit ng mga aralin at tanong sa pagsusulit.
- **Dual Persistence (Online + Offline)**: Gumagana gamit ang Firebase Firestore (kung may cloud configuration) o automatic `localStorage` fallback (gumagana kahit static hosting o walang backend).

---

## 🚀 Paano I-publish (Publishing Guide)

Piliin ang pinakamadaling paraan para sa iyo:

### Paraan 1: GitHub Pages (Inirerekomenda - Libre at Permanente)
1. Pumunta sa [github.com/new](https://github.com/new) at gumawa ng bagong repository (hal. `ap7-imperyalistang-hapon`).
2. Sa iyong terminal sa folder na ito, patakbuhin ang sumusunod:
   ```bash
   git remote add origin https://github.com/IYONG-USERNAME/ap7-imperyalistang-hapon.git
   git branch -M main
   git push -u origin main
   ```
3. Sa GitHub repository, pumunta sa **Settings** > **Pages**.
4. Sa ilalim ng **Build and deployment** > **Branch**, piliin ang `main` at `/ (root)`, pagkatapos ay i-click ang **Save**.
5. Pagkatapos ng 1-2 minuto, mabubuksan na ang laro sa:
   `https://IYONG-USERNAME.github.io/ap7-imperyalistang-hapon/`

---

### Paraan 2: Netlify Drop (Pinakamabilis - Walang kailangang i-type)
1. Buksan ang [app.netlify.com/drop](https://app.netlify.com/drop) sa iyong browser.
2. I-drag at i-drop ang buong folder na ito (`AP7 - Imperyalistang Japan Interactive Game`) sa kahon.
3. Agad kang bibigyan ng live public URL (hal. `https://ap7-japan-quest.netlify.app`) na puwede nang ipamahagi sa mga mag-aaral!

---

### Paraan 3: Vercel
1. I-install ang Vercel CLI o mag-login sa [vercel.com](https://vercel.com).
2. Mag-import gamit ang GitHub repository o patakbuhin sa terminal:
   ```bash
   npx vercel
   ```
3. Piliin ang defaults, at live na ang iyong modyul sa loob ng 30 segundo.

---

### Paraan 4: Pagpapatakbo sa Classroom Local Network (Offline / Wi-Fi)
Kung nais gamitin sa classroom na walang internet o mabagal ang koneksyon:
1. Sa terminal, patakbuhin:
   ```bash
   python -m http.server 8080
   ```
2. Hanapin ang iyong Local IP address (gamit ang `ipconfig` sa command prompt).
3. Puwede nang kumonekta ang mga mag-aaral sa parehong Wi-Fi sa pamamagitan ng browser gamit ang:
   `http://192.168.x.x:8080`

---

## 📁 Estruktura ng Proyekto
- `index.html` - Pangunahing web application (entry point para sa hosting).
- `interactive_online_learning_module.html` - Orihinal na source file.
- `README.md` - Dokumentasyon at gabay sa pag-publish.
- `.gitignore` - Mga pansamantalang file na hindi kailangang i-upload.
