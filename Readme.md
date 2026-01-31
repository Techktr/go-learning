# Go Learning Path - Projets

> 🚧 **Learning in progress** - Ce repo documente mon apprentissage de Go.
> Le code n'est pas production-ready, je suis en train d'apprendre !

## 🚀 Projets en cours

### myps - Clone de `ps`
**Status:** Tests unitaires à finir
**Concepts:** `/proc` filesystem, parsing, CLI
**Repo:** https://github.com/Techktr/myps

### rpg-game (Ebiten)
**Status:** Phase 1 terminée (mouvement, gravité, plateformes)
**Concepts:** Game dev, physique 2D, architecture
**Repo:** [lien GitHub à ajouter]

---

## 📋 Prochains projets (Court terme)

### 1. Container Runtime (mini-Docker)
**Difficulté:** ⭐⭐⭐⭐
**Durée estimée:** 2-3 soirées
**Concepts clés:**
- Linux namespaces (PID, mount, network)
- Cgroups (limitation ressources)
- Syscalls (`clone()`, `chroot()`, `pivot_root()`)
- Filesystem isolation

**Phases:**
1. Namespace PID basique
2. Filesystem isolé (chroot)
3. Cgroups (limites RAM/CPU)
4. Réseau (optionnel)

**Ressources:**
- `/proc/<pid>/ns/*`
- `/sys/fs/cgroup/`
- `man 2 clone`
- `man 2 unshare`

---

### 2. Message Broker (mini-Kafka/RabbitMQ)
**Difficulté:** ⭐⭐⭐
**Durée estimée:** 1 week-end
**Concepts clés:**
- Réseau TCP (`net.Listen()`, `net.Dial()`)
- Channels Go (queues thread-safe)
- Persistence (append-only log)
- Pub/Sub pattern

**Phases:**
1. Serveur TCP basique
2. Queue en mémoire (channel)
3. Publisher/Consumer
4. Persistence sur disque
5. Multiple topics/partitions (optionnel)

**Ressources:**
- Package `net`
- Channels Go
- File I/O

---

## 🎨 Projets GUI (Fyne)

### 3. Jeu de la Vie avec GUI
**Difficulté:** ⭐⭐
**Durée estimée:** 1 soirée
**Concepts clés:**
- Fyne basics (window, canvas, buttons)
- Animation/refresh
- UI controls (play/pause, speed slider)

**Features:**
- Grille visuelle
- Boutons play/pause/reset
- Slider vitesse
- Load patterns (glider, blinker)

---

### 4. Visualiseur d'algorithmes de tri
**Difficulté:** ⭐⭐⭐
**Durée estimée:** 2 soirées
**Concepts clés:**
- Fyne canvas drawing
- Goroutines (animation)
- Algos de tri (quicksort, merge, bubble)

**Features:**
- Barres animées
- Comparaison de perfs
- Step-by-step mode

---

### 5. System Monitor GUI
**Difficulté:** ⭐⭐⭐
**Durée estimée:** 1 week-end
**Concepts clés:**
- Lecture `/proc` (comme myps)
- Fyne widgets (graphs, labels)
- Real-time updates

**Features:**
- CPU/RAM/Disk usage
- Process list
- Graphs temps réel
- Kill process

---

## 🛠️ Outils système (CLI)

### 6. Clone de `htop`
**Difficulté:** ⭐⭐⭐⭐
**Durée estimée:** 1 semaine
**Concepts clés:**
- Terminal UI (termbox-go ou tview)
- `/proc` parsing avancé
- Tri/filtrage processus
- Refresh automatique

---

### 7. Clone de `tree`
**Difficulté:** ⭐⭐
**Durée estimée:** 1 soirée
**Concepts clés:**
- Filesystem recursion
- String formatting (box-drawing chars)
- CLI flags

---

### 8. Log analyzer
**Difficulté:** ⭐⭐
**Durée estimée:** 1 soirée
**Concepts clés:**
- File parsing
- Regex
- Colored output
- Filtering/searching

---

## 🔥 Projets ambitieux (Long terme)

### 9. Mini shell
**Difficulté:** ⭐⭐⭐⭐⭐
**Concepts clés:**
- Parsing de commandes
- Pipes, redirections
- Built-ins (cd, export, etc.)
- Job control

---

### 10. Compilateur/Interpréteur
**Difficulté:** ⭐⭐⭐⭐⭐
**Concepts clés:**
- Lexer/Parser
- AST (Abstract Syntax Tree)
- Interpreter pattern
- REPL

---

## 📚 Compétences à acquérir

- [x] Tests unitaires (myps)
- [ ] Fyne GUI
- [x] Ebiten game dev (en cours)
- [ ] Réseau TCP/UDP
- [ ] Syscalls Linux avancés
- [ ] Concurrency (goroutines, channels)
- [ ] Performance profiling
- [ ] Docker internals
- [ ] Message queues

---

## 🎯 Progression

**Mois 1 (Janvier 2026):**
- ✅ myps (code fait, tests restants)
- ✅ Jeu de la Vie (console)
- ✅ rpg-game Ebiten (Phase 1)
- 🔄 Container runtime (à commencer)

**Mois 2 (Février 2026):**
- [x] Finir tests myps
- [ ] Container runtime complet
- [ ] Message broker basique
- [ ] Jeu de la Vie + Fyne

---

## 💡 Notes

**Ordre recommandé:**
1. Finir tests myps (consolider les bases)
2. Container runtime (syscalls Linux)
3. Message broker (réseau + queues)
4. Projets Fyne (GUI)
5. Projets ambitieux

**Philosophie:**
- Tout est fichier
- Pas de magie, que des syscalls
- Commencer simple, itérer
- Comprendre avant d'optimiser

**Ressources:**
- Livres Go (arrivée 30 janvier)
- `/proc` filesystem
- `man 2 clone` (syscalls)
- Fyne docs
- NATS source code (message broker en Go)

---

## 🧠 Réalisations importantes

**Ce qui a changé en 1 mois:**

```
Avant : "C'est de la magie"
        ↓
Maintenant : "C'est juste des fichiers et des syscalls"
        ↓
Bientôt : "J'ai fait mon propre container runtime"
        ↓
Plus tard : "Je comprends les trade-offs de Docker"
```

**Déclic principal:**
- Docker = syscalls Linux (`clone()`, `chroot()`, cgroups)
- Kafka = TCP + fichiers + queue
- Réseau = `net.Listen()` / `net.Dial()`
- Containers = namespaces + isolation

**Tout est faisable. Il suffit de déconstruire la complexité.**
