Comprovar els remotes que tens per assegurar-te que tot està ben configurat:
git remote -v
Hauries de veure quelcom així:

origin    https://github.com/el-teu-usuari/directus.git (fetch)
origin    https://github.com/el-teu-usuari/directus.git (push)
upstream  https://github.com/directus/directus.git (fetch)
upstream  https://github.com/directus/directus.git (push)
Per rebre els canvis del projecte original (és a dir, de upstream):
git fetch upstream
git checkout main            # o la branca principal que prefereixis
git merge upstream/main
(o bé un git rebase si prefereixes un historial més lineal).
Resol els conflictes si n’hi ha, i un cop tinguis tot resolt, fes commit i push a la teva fork:
git push origin main
Això et permet mantenir els canvis que has fet (els tens al teu repositori, i de fet en pots crear branques específiques per als teus canvis), alhora que importes els canvis del repositori principal.