# DeepForum – Kuratiertes Diskussions- & News-Forum

## 🧱 Projektstruktur (MVP-Basis)

```
📁 deepforum/
├── .github/workflows/             # CI/CD mit Jenkins Triggern (optional GitHub Actions)
├── backend/
│   ├── src/
│   │   ├── controllers/
│   │   ├── models/
│   │   ├── routes/
│   │   └── index.ts               # Express Server
│   ├── .env
│   ├── package.json
│   └── tsconfig.json
├── frontend/
│   ├── components/
│   ├── pages/
│   ├── public/
│   ├── styles/
│   ├── utils/
│   ├── next.config.js
│   └── tsconfig.json
├── docker/
│   ├── Dockerfile.backend
│   ├── Dockerfile.frontend
│   └── docker-compose.yml
├── docs/
│   └── postman_collection.json    # API Doku / Beispielaufrufe
├── .env
├── README.md                     # Projektbeschreibung
└── LICENSE
```

## ⚙️ CI/CD + DevOps
- Jenkinsfile für Build + Deploy auf eigenen VPS
- Docker-Container (Node Backend, Next Frontend)
- Reverse Proxy via nginx optional

## 🧩 Backend Stack (Node.js + Express + MongoDB)
- Auth: JWT + Refresh Token (Login, Register, Rollen)
- Models: User, Thread, Post, Topic, ArchivedThread
- APIs: REST-Endpoints, geschützt via Middleware
- Tools: Postman Collection, MongoDB Compass

## 🧩 Frontend Stack (Next.js + Tailwind)
- Seiten: Home, Topics, ThreadView, New Post, Login/Register
- Auth: Persistenter Login via Context/Storage
- UI: Minimalistisch, Fokus auf Lesbarkeit + Struktur

## 🔐 Authentifizierung
- User mit Rollen: Gast, User, Moderator, Admin
- Auth-Flow: Register/Login → Token → API Access

## 📚 Dokumentation
- Postman Collection mit Beispiel-Requests
- GitHub Pages für Dev-Doku + Wiki geplant

## 🧪 Tests & Dev
- Lokales Setup mit `docker-compose up`
- Tests (später): Jest + Cypress

---

## 📌 To Do (für nächste Schritte)
- [ ] CI/CD Setup (Jenkinsfile + Deploy-Test)
- [ ] Docker Compose zum Laufen bringen
- [ ] Grundrouten im Backend definieren
- [ ] Auth + MongoDB-Anbindung
- [ ] Thread/Topic Modell + erste API
- [ ] Frontend: Login-Flow + Forum-Startseite (MVP)

---

## 📌 Hinweis
> 📌 Hinweis: Dieses Repository ist **öffentlich einsehbar**, aber **nicht Open Source**.  
> Eine **Nutzung, Veränderung oder Weitergabe ist ausschließlich mit schriftlicher Genehmigung** des Eigentümers erlaubt.  
> Der Inhalt dieses README ist **nicht final** und wird regelmäßig erweitert.

---

## 📝 Lizenz
Dieses Projekt unterliegt einer benutzerdefinierten Lizenz.  
Details findest du in der Datei [LICENSE.md](./LICENSE.md).  
**Eine Nutzung oder Verbreitung ist nur mit ausdrücklicher Genehmigung erlaubt.**

---

⏳ Dieses Dokument wird regelmäßig überarbeitet.  
Letzte Bearbeitung: 01.08.2025
