DEEP Windows Worker Package
--------------------------------
Files:
  - start-worker.ps1  : creates the worker at your custom path and starts it
  - worker-win.js     : the worker code (also embedded into the PS1 if missing)
  - start-tunnel.ps1  : opens SSH reverse tunnels 18089 (proxy) and 19321 (renderer)

Usage:
  1) Run PowerShell as Administrator (optional but recommended).
  2) Double-click start-tunnel.ps1 (or run in an open PS window) to open reverse tunnels.
  3) Run start-worker.ps1. It will create the folder:
       C:\Users\Makkaroshka\Desktop\DEEP Первое. Шаг 3. Мини-очередь сервер-блокер Windows
     and start the worker with env SERVER_BASE/RENDER_BASE/TOKEN.
  4) On the server, check queue stats:  curl -sS http://127.0.0.1:9101/queue/stats

Edit inside PS1 if your server IP/port differ.
