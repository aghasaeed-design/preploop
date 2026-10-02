# PrepLoop

Static site: upload `index.html` to the root of a GitHub repo.

## Publish
1. Repo > Settings > Pages > Deploy from branch > `main` / root.
2. Custom domain: enter your domain in Pages settings (GitHub creates a `CNAME` file).
3. At your DNS provider add `A` records for the apex domain: 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153, and a `CNAME` for `www` pointing to `<username>.github.io`.
4. Tick "Enforce HTTPS" once the certificate is ready.

## Add more questions
Edit the `Q` array in `index.html`: `[exam, topic, question, [options], correctIndex, explanation]`.

## Shared community
Posts and scores are stored in each visitor's browser. For shared posts, accounts and a real leaderboard, connect Firebase (Auth + Firestore) and replace the `S.posts` reads and writes.
