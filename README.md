<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>

<title>IrrigaTech Dashboard</title>

<link rel="stylesheet"
href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.2/css/all.min.css"/>

<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>

<style>

/* ═══════════════════════════════════════
   RESET
═══════════════════════════════════════ */

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

:root{

    --bg:#f0f4f8;
    --surface:#ffffff;
    --surface2:#f8fafc;

    --border:#e2e8f0;

    --txt:#0f172a;
    --txt2:#475569;
    --txt3:#94a3b8;

    --green:#16a34a;
    --green-dark:#15803d;

    --yellow:#d97706;

    --red:#dc2626;

    --blue:#2563eb;

    --shadow:
    0 5px 18px rgba(0,0,0,0.06);

    --radius:18px;
}

body{
    font-family:Arial, Helvetica, sans-serif;
    background:var(--bg);
    color:var(--txt);
}

/* ═══════════════════════════════════════
   HEADER
═══════════════════════════════════════ */

.site-header{

    height:75px;

    background:#0f172a;

    color:white;

    display:flex;
    align-items:center;
    justify-content:space-between;

    padding:0 30px;

    position:sticky;
    top:0;
    z-index:999;

    box-shadow:0 4px 15px rgba(0,0,0,0.2);
}

.header-brand{
    display:flex;
    align-items:center;
    gap:15px;
}

.brand-logo{
    width:48px;
    height:48px;
}

.brand-name{
    font-size:22px;
    font-weight:800;
}

.brand-sub{
    font-size:12px;
    color:#94a3b8;
}

.conn-pill{

    display:flex;
    align-items:center;
    gap:10px;

    background:rgba(255,255,255,0.1);

    padding:10px 18px;

    border-radius:999px;

    font-size:14px;
}

.conn-dot{

    width:10px;
    height:10px;

    border-radius:50%;

    background:#22c55e;

    animation:pulse 1.5s infinite;
}

.clock-time{
    font-size:18px;
    font-weight:bold;
}

.clock-date{
    font-size:12px;
    color:#94a3b8;
}

.main{
    max-width:1600px;
    margin:auto;
    padding:30px;
}

.section{
    margin-bottom:30px;
}

.section-head{

    display:flex;
    align-items:center;
    justify-content:space-between;

    margin-bottom:20px;
}

.section-title{

    display:flex;
    align-items:center;
    gap:10px;

    font-size:15px;
    font-weight:800;

    color:var(--txt2);

    text-transform:uppercase;
}

.site-footer{

    margin-top:40px;

    background:white;

    border-top:1px solid #e2e8f0;

    padding:20px 30px;

    display:flex;
    justify-content:space-between;

    color:#64748b;
}

@keyframes pulse{

    0%{
        box-shadow:0 0 0 0 rgba(34,197,94,0.6);
    }

    70%{
        box-shadow:0 0 0 12px rgba(34,197,94,0);
    }

    100%{
        box-shadow:0 0 0 0 rgba(34,197,94,0);
    }
}

@media(max-width:768px){

    .site-header{

        flex-direction:column;

        height:auto;

        padding:20px;

        gap:15px;
    }

    .main{
        padding:20px;
    }

    .site-footer{

        flex-direction:column;

        text-align:center;

        gap:10px;
    }
}

</style>
</head>

<body>

<header class="site-header">

<div class="header-brand">

<div class="brand-logo">

<svg viewBox="0 0 64 64" fill="none">

<circle
cx="32"
cy="32"
r="30"
fill="#16a34a"/>

<path
d="M20 38L30 26L40 34L48 22"
stroke="white"
stroke-width="4"/>

</svg>

</div>

<div>

<div class="brand-name">
IrrigaTech
</div>

<div class="brand-sub">
Sistema Inteligente de Irrigação
</div>

</div>

</div>

<div class="conn-pill">

<div class="conn-dot"></div>

Sistema Online

</div>

<div>

<div class="clock-time" id="clock"></div>

<div class="clock-date" id="date"></div>

</div>

</header>

<main class="main">

<section class="section">

<div class="section-head">

<div class="section-title">

<i class="fa-solid fa-chart-line"></i>

Monitoramento em Tempo Real

</div>

</div>

<p style="font-size:18px;color:#475569;">
Dashboard agrícola inteligente com monitoramento de irrigação e energia solar.
</p>

</section>

</main>

<footer class="site-footer">

<span>
IrrigaTech © 2026
</span>

<span>
Sistema Inteligente de Irrigação Solar
</span>

</footer>

<script>

function updateClock(){

    const now = new Date();

    document.getElementById("clock").innerHTML =
    now.toLocaleTimeString("pt-BR");

    document.getElementById("date").innerHTML =
    now.toLocaleDateString("pt-BR");
}

setInterval(updateClock,1000);

updateClock();

</script>

</body>
</html>
