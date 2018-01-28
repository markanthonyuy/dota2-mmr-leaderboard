# Dota 2 MMR Leaderboard
Dota 2 MMR Leaderboard

## Dev notes

### Cronjobs
```bash
0 */6 * * * get-mmr-leaderboard.sh
0 */6 * * * cd  ~/Documents/projects/scraper/dota2/mmr-leaderboard/ && npm run build && cd build && ./autocommit.sh
```

#### get-mmr-leaderboard.sh
```bash
#!/usr/bin/env sh
/home/administrator/.nvm/versions/node/v8.6.0/bin/node /home/administrator/Documents/projects/scraper/dota2-leaderboard.js
```

#### autocommit.sh
(This file is generated in npm run build script, Make sure to use and configure ssh, Make sure it excecutable)
```bash
git init; git remote add origin git@github.com:markanthonyuy/dota2-mmr-leaderboard.git; git add -A .; git commit -m "update" .; git push origin master -f
```
