<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>TUCADI – Renta de Locales Comerciales en Hermosillo</title>
<link href="https://fonts.googleapis.com/css2?family=Lora:ital,wght@0,500;0,600;0,700;1,500&family=Plus+Jakarta+Sans:wght@300;400;500;600;700&display=swap" rel="stylesheet">
<style>
:root{
  --bg:#faf8f4;--surface:#fff;--warm:#f5f0e8;--border:#e8e2d8;--border2:#d4ccbe;
  --text:#1e1a14;--muted:#7a7060;--soft:#a89880;
  --accent:#1a4fc4;--accent-l:#e8effe;--accent-ll:#f0f4ff;
  --accent2:#0e3499;--accent2-l:#e4ebff;
  --blue:#3060a8;--blue-l:#e8eef8;
  --purple:#6840c0;--purple-l:#f0ecfa;
  --r:10px;--rl:16px;--rxl:22px;
  --sh:0 1px 3px rgba(30,26,20,.06),0 4px 16px rgba(30,26,20,.07);
  --sh2:0 2px 8px rgba(30,26,20,.05),0 12px 40px rgba(30,26,20,.13);
}
*{box-sizing:border-box;margin:0;padding:0}
body{font-family:'Plus Jakarta Sans',sans-serif;background:var(--bg);color:var(--text);min-height:100vh;overflow-x:hidden}

/* NAV */
nav{display:flex;align-items:center;justify-content:space-between;padding:0 2.5rem;height:62px;background:var(--surface);border-bottom:1px solid var(--border);position:sticky;top:0;z-index:200;box-shadow:0 1px 0 var(--border)}
.logo{font-family:'Plus Jakarta Sans',sans-serif;font-weight:800;font-size:1.25rem;color:var(--text);text-decoration:none;letter-spacing:.04em}
.logo em{color:var(--accent);font-style:normal;letter-spacing:.04em}

.nav-links{display:flex;gap:1.8rem}
.nav-links a{color:var(--muted);text-decoration:none;font-size:.88rem;font-weight:500;transition:color .18s}
.nav-links a:hover{color:var(--accent)}
.nav-actions{display:flex;gap:.75rem;align-items:center}
.btn-out{background:none;border:1.5px solid var(--border2);color:var(--text);padding:.42rem 1rem;border-radius:8px;font-family:'Plus Jakarta Sans',sans-serif;font-size:.83rem;font-weight:600;cursor:pointer;transition:all .18s}
.btn-out:hover{border-color:var(--accent);color:var(--accent)}
.btn-prim{background:var(--accent);color:#fff;border:none;padding:.45rem 1.1rem;border-radius:8px;font-family:'Plus Jakarta Sans',sans-serif;font-size:.83rem;font-weight:600;cursor:pointer;transition:background .18s}
.btn-prim:hover{background:#1240a8}

/* HERO */
.hero{background:var(--surface);border-bottom:1px solid var(--border);overflow:hidden}
.hero-inner{max-width:1140px;margin:0 auto;padding:3.5rem 2.5rem 0;display:grid;grid-template-columns:1fr 400px;gap:2.5rem;align-items:end}
.hero-eyebrow{display:inline-flex;align-items:center;gap:7px;background:var(--accent-l);color:var(--accent);font-size:.72rem;font-weight:700;letter-spacing:.07em;text-transform:uppercase;padding:.3rem .85rem;border-radius:100px;border:1px solid #b0c8f8;margin-bottom:1.2rem}
.hero-eyebrow::before{content:"";width:7px;height:7px;border-radius:50%;background:var(--accent);flex-shrink:0}
.hero h1{font-family:'Lora',serif;font-size:clamp(1.9rem,3.8vw,2.9rem);font-weight:700;line-height:1.2;margin-bottom:.9rem}
.hero h1 i{color:var(--accent);font-style:italic}
.hero-sub{color:var(--muted);font-size:.95rem;line-height:1.72;max-width:460px;margin-bottom:1.8rem}
.hero-search{display:flex;gap:.6rem;margin-bottom:1.5rem}
.hero-search input{flex:1;background:var(--warm);border:1.5px solid var(--border);color:var(--text);padding:.68rem 1rem;border-radius:10px;font-family:'Plus Jakarta Sans',sans-serif;font-size:.9rem;outline:none;transition:border .2s}
.hero-search input:focus{border-color:var(--accent);background:#fff}
.hero-search input::placeholder{color:var(--soft)}
.btn-sh{background:var(--accent);color:#fff;border:none;padding:.68rem 1.4rem;border-radius:10px;font-family:'Plus Jakarta Sans',sans-serif;font-size:.9rem;font-weight:700;cursor:pointer;white-space:nowrap;transition:background .18s}
.btn-sh:hover{background:#1240a8}
.chips{display:flex;flex-wrap:wrap;gap:.45rem;margin-bottom:2.5rem}
.chip{background:var(--warm);border:1px solid var(--border);color:var(--muted);font-size:.75rem;font-weight:600;padding:.26rem .72rem;border-radius:100px;cursor:pointer;transition:all .18s}
.chip:hover,.chip.on{background:var(--accent-l);border-color:#b0c8f8;color:var(--accent)}
.hero-stats{display:flex;border-top:1px solid var(--border);margin:0 -2.5rem}
.hst{flex:1;padding:1.1rem 1.5rem;border-right:1px solid var(--border);text-align:center}
.hst:last-child{border-right:none}
.hst-n{font-family:'Lora',serif;font-size:1.5rem;font-weight:700;color:var(--accent)}
.hst-l{color:var(--muted);font-size:.68rem;font-weight:600;text-transform:uppercase;letter-spacing:.05em;margin-top:2px}
.hero-illo svg{width:100%;display:block}

/* FILTERS */
.fw{max-width:1140px;margin:0 auto;padding:1.4rem 2.5rem}
.fc{background:var(--surface);border:1px solid var(--border);border-radius:var(--rl);padding:1.1rem 1.3rem;box-shadow:var(--sh);display:flex;flex-wrap:wrap;gap:.85rem;align-items:flex-end}
.fg{display:flex;flex-direction:column;gap:.28rem;flex:1;min-width:125px}
.fg label{font-size:.67rem;color:var(--muted);text-transform:uppercase;letter-spacing:.07em;font-weight:700}
.fg select,.fg input{background:var(--warm);border:1.5px solid var(--border);color:var(--text);padding:.5rem .78rem;border-radius:8px;font-family:'Plus Jakarta Sans',sans-serif;font-size:.86rem;font-weight:500;outline:none;transition:border .2s;-webkit-appearance:none}
.fg select:focus,.fg input:focus{border-color:var(--accent);background:#fff}
.btn-fil{background:var(--accent);color:#fff;border:none;padding:.52rem 1.3rem;border-radius:8px;font-family:'Plus Jakarta Sans',sans-serif;font-size:.88rem;font-weight:700;cursor:pointer;white-space:nowrap;align-self:flex-end;transition:background .18s}
.btn-fil:hover{background:#1240a8}
.btn-cl{display:flex;align-items:center;gap:.45rem;color:var(--muted);font-size:.8rem;font-weight:600;cursor:pointer;padding:.52rem .78rem;border:1.5px solid var(--border);border-radius:8px;background:var(--warm);align-self:flex-end;white-space:nowrap;transition:all .18s}
.btn-cl:hover{border-color:var(--accent);color:var(--accent)}

/* SECTION */
.sec{max-width:1140px;margin:0 auto;padding:2rem 2.5rem 3rem}
.sec-head{display:flex;justify-content:space-between;align-items:center;margin-bottom:1.3rem;flex-wrap:wrap;gap:.8rem}
.sec-title{font-family:'Lora',serif;font-size:1.22rem;font-weight:700}
.sort-row{display:flex;gap:.45rem;align-items:center}
.sort-lbl{font-size:.76rem;color:var(--muted);font-weight:600}
.sb{font-size:.75rem;padding:.26rem .65rem;border-radius:6px;border:1px solid var(--border);background:var(--warm);color:var(--muted);cursor:pointer;font-family:'Plus Jakarta Sans',sans-serif;font-weight:600;transition:all .18s}
.sb:hover,.sb.on{background:var(--accent-l);border-color:#b0c8f8;color:var(--accent)}
.pill{background:var(--accent-l);color:var(--accent);font-size:.73rem;font-weight:700;padding:.23rem .72rem;border-radius:100px}

/* GRID */
.grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(320px,1fr));gap:1.35rem}
.card{background:var(--surface);border:1px solid var(--border);border-radius:var(--rl);overflow:hidden;box-shadow:var(--sh);transition:box-shadow .25s,transform .25s;cursor:pointer}
.card:hover{box-shadow:var(--sh2);transform:translateY(-4px)}
.cthumb{height:178px;position:relative;overflow:hidden}
.cthumb svg{width:100%;height:100%}
.cthumb-ov{position:absolute;inset:0;background:linear-gradient(to bottom,transparent 55%,rgba(30,26,20,.15))}
.bdg{position:absolute;top:11px;left:11px;font-size:.68rem;font-weight:700;text-transform:uppercase;letter-spacing:.05em;padding:.26rem .62rem;border-radius:5px}
.bdg-new{background:var(--accent);color:#fff}
.bdg-hot{background:#c0391a;color:#fff}
.bdg-ok{background:rgba(255,255,255,.92);color:var(--accent);border:1px solid #b0c8f8}
.cfav{position:absolute;top:10px;right:10px;width:32px;height:32px;border-radius:50%;background:rgba(255,255,255,.88);border:1px solid var(--border);display:flex;align-items:center;justify-content:center;cursor:pointer;font-size:.9rem;transition:transform .18s;box-shadow:0 1px 4px rgba(0,0,0,.1)}
.cfav:hover{transform:scale(1.12)}
.cfav.on{background:#fff2f2}
.cviews{position:absolute;bottom:9px;right:9px;background:rgba(255,255,255,.85);border:1px solid var(--border);border-radius:5px;font-size:.68rem;font-weight:600;padding:.18rem .5rem;color:var(--muted)}
.cbody{padding:1rem 1.1rem}
.ctop{display:flex;justify-content:space-between;align-items:flex-start;margin-bottom:.45rem}
.czona{font-size:.7rem;color:var(--muted);font-weight:700;text-transform:uppercase;letter-spacing:.06em}
.crat{display:flex;align-items:center;gap:3px;font-size:.73rem;font-weight:700;color:#c07818}
.cname{font-family:'Lora',serif;font-weight:700;font-size:.98rem;line-height:1.35;margin-bottom:.6rem}
.ctags{display:flex;flex-wrap:wrap;gap:4px;margin-bottom:.8rem}
.tag{font-size:.68rem;font-weight:600;padding:.2rem .55rem;border-radius:4px}
.tg{background:var(--accent-l);color:var(--accent);border:1px solid #b0c8f8}
.to{background:var(--accent2-l);color:var(--accent2);border:1px solid #e8c4a0}
.tb{background:var(--blue-l);color:var(--blue);border:1px solid #b8ccee}
.tp{background:var(--purple-l);color:var(--purple);border:1px solid #ccc0f0}
.tx{background:var(--warm);color:var(--muted);border:1px solid var(--border)}
.cspecs{display:grid;grid-template-columns:1fr 1fr;gap:.4rem .8rem;margin-bottom:.85rem;font-size:.78rem;color:var(--muted)}
.cs{display:flex;align-items:center;gap:4px}
.sv{color:var(--text);font-weight:600}
.cfoot{display:flex;justify-content:space-between;align-items:center;padding-top:.8rem;border-top:1px solid var(--border)}
.cprice{font-family:'Lora',serif;font-weight:700;font-size:1.18rem;color:var(--accent)}
.cprice small{font-family:'Plus Jakarta Sans',sans-serif;font-size:.68rem;color:var(--muted);font-weight:400}
.cpm2{font-size:.7rem;color:var(--soft);margin-top:1px}
.btn-ver{background:var(--accent-l);border:1px solid #b0c8f8;color:var(--accent);padding:.38rem .95rem;border-radius:6px;font-size:.78rem;font-weight:700;cursor:pointer;transition:all .2s;font-family:'Plus Jakarta Sans',sans-serif}
.btn-ver:hover{background:var(--accent);color:#fff;border-color:var(--accent)}

/* HOW IT WORKS */
.how{background:var(--surface);border-top:1px solid var(--border);border-bottom:1px solid var(--border);padding:3.2rem 2.5rem}
.how-in{max-width:1140px;margin:0 auto}
.how h2{font-family:'Lora',serif;font-size:1.55rem;font-weight:700;text-align:center;margin-bottom:.4rem}
.how-sub{text-align:center;color:var(--muted);font-size:.9rem;margin-bottom:2.8rem}
.how-steps{display:grid;grid-template-columns:repeat(4,1fr);gap:1.2rem}
.step{text-align:center;padding:1.4rem .9rem;position:relative}
.step:not(:last-child)::after{content:"→";position:absolute;right:-14px;top:28px;color:var(--border2);font-size:1.1rem}
.step-ico{font-size:1.5rem;margin-bottom:.65rem;display:block}
.step-n{width:40px;height:40px;border-radius:50%;background:var(--accent);color:#fff;font-family:'Lora',serif;font-size:1rem;font-weight:700;display:inline-flex;align-items:center;justify-content:center;margin-bottom:.75rem}
.step h3{font-family:'Lora',serif;font-size:.95rem;font-weight:700;margin-bottom:.35rem}
.step p{color:var(--muted);font-size:.81rem;line-height:1.65}

/* ZONAS */
.zonas{border-top:1px solid var(--border);border-bottom:1px solid var(--border);padding:2.2rem 2.5rem;background:var(--warm)}
.zonas-in{max-width:1140px;margin:0 auto}
.zonas-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(148px,1fr));gap:.85rem;margin-top:1.2rem}
.zchip{background:var(--surface);border:1.5px solid var(--border);border-radius:var(--r);padding:.8rem .9rem;cursor:pointer;transition:all .2s;text-align:center}
.zchip:hover{border-color:var(--accent);background:var(--accent-ll)}
.zchip-name{font-weight:700;font-size:.85rem;margin-bottom:.18rem}
.zchip-cnt{font-size:.7rem;color:var(--muted)}

/* TESTIMONIOS */
.testi{max-width:1140px;margin:0 auto;padding:2.8rem 2.5rem}
.testi h2{font-family:'Lora',serif;font-size:1.35rem;font-weight:700;margin-bottom:.35rem}
.testi-sub{color:var(--muted);font-size:.86rem;margin-bottom:1.8rem}
.tgrid{display:grid;grid-template-columns:repeat(3,1fr);gap:1.1rem}
.tc{background:var(--surface);border:1px solid var(--border);border-radius:var(--rl);padding:1.3rem;box-shadow:var(--sh)}
.tc-stars{color:#e09010;font-size:.9rem;margin-bottom:.7rem;letter-spacing:2px}
.tc-text{font-size:.85rem;line-height:1.72;color:var(--text);margin-bottom:.95rem;font-style:italic}
.tc-auth{display:flex;align-items:center;gap:.7rem}
.tc-av{width:36px;height:36px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-weight:700;font-size:.82rem;flex-shrink:0}
.tc-info strong{font-size:.85rem;font-weight:700;display:block}
.tc-info small{font-size:.7rem;color:var(--muted)}

/* CTA */
.cta-w{max-width:1140px;margin:2rem auto 3rem;padding:0 2.5rem}
.cta-box{background:var(--accent);border-radius:var(--rxl);padding:2.6rem 3rem;display:flex;justify-content:space-between;align-items:center;gap:2rem;flex-wrap:wrap;position:relative;overflow:hidden}
.cta-box::before{content:"";position:absolute;right:-50px;top:-50px;width:240px;height:240px;border-radius:50%;background:rgba(255,255,255,.07)}
.cta-box::after{content:"";position:absolute;right:70px;bottom:-70px;width:160px;height:160px;border-radius:50%;background:rgba(255,255,255,.05)}
.cta-txt{position:relative}
.cta-txt h2{font-family:'Lora',serif;font-size:1.65rem;font-weight:700;color:#fff;margin-bottom:.45rem;line-height:1.25}
.cta-txt p{color:rgba(255,255,255,.75);font-size:.9rem;max-width:380px}
.btn-cta{background:#fff;color:var(--accent);border:none;padding:.82rem 1.9rem;border-radius:10px;font-family:'Plus Jakarta Sans',sans-serif;font-size:.92rem;font-weight:700;cursor:pointer;white-space:nowrap;flex-shrink:0;position:relative;transition:opacity .2s}
.btn-cta:hover{opacity:.9}

/* FOOTER */
footer{background:var(--surface);border-top:1px solid var(--border);padding:2.4rem 2.5rem 1.4rem}
.ft-in{max-width:1140px;margin:0 auto}
.ft-top{display:grid;grid-template-columns:1.5fr 1fr 1fr 1fr;gap:2rem;margin-bottom:2rem}
.ft-brand p{color:var(--muted);font-size:.8rem;line-height:1.65;margin-top:.55rem;max-width:210px}
.ft-col h4{font-weight:700;font-size:.78rem;margin-bottom:.85rem;text-transform:uppercase;letter-spacing:.06em}
.ft-col a{display:block;color:var(--muted);text-decoration:none;font-size:.8rem;margin-bottom:.45rem;transition:color .18s}
.ft-col a:hover{color:var(--accent)}
.ft-bot{border-top:1px solid var(--border);padding-top:1.1rem;display:flex;justify-content:space-between;align-items:center;flex-wrap:wrap;gap:.5rem}
.ft-bot p{color:var(--soft);font-size:.76rem}
.ft-bdg{background:var(--accent-l);color:var(--accent);font-size:.68rem;font-weight:700;padding:.18rem .55rem;border-radius:4px}

/* MODAL */
.ov{position:fixed;inset:0;z-index:500;background:rgba(20,16,10,.48);display:flex;align-items:center;justify-content:center;padding:1.5rem;opacity:0;pointer-events:none;transition:opacity .22s}
.ov.open{opacity:1;pointer-events:all}
.modal{background:var(--surface);border-radius:var(--rxl);width:100%;max-width:610px;max-height:90vh;overflow-y:auto;box-shadow:0 24px 80px rgba(20,16,10,.22);transform:translateY(20px);transition:transform .22s}
.ov.open .modal{transform:translateY(0)}
.m-thumb{height:195px;position:relative;border-radius:var(--rxl) var(--rxl) 0 0;overflow:hidden}
.m-thumb svg{width:100%;height:100%}
.m-close{position:absolute;top:12px;right:12px;width:30px;height:30px;border-radius:50%;background:rgba(255,255,255,.9);border:1px solid var(--border);color:var(--muted);cursor:pointer;display:flex;align-items:center;justify-content:center;font-size:.85rem;transition:all .18s;z-index:10}
.m-close:hover{background:#fff;color:var(--text)}
.m-body{padding:1.7rem 1.9rem}
.m-zona{font-size:.7rem;font-weight:700;text-transform:uppercase;letter-spacing:.07em;color:var(--muted);margin-bottom:.35rem}
.m-name{font-family:'Lora',serif;font-size:1.4rem;font-weight:700;line-height:1.25;margin-bottom:.3rem}
.m-rating{display:flex;align-items:center;gap:6px;margin-bottom:1.2rem;font-size:.8rem;color:var(--muted)}
.m-stars{color:#e09010;letter-spacing:2px}
.m-price-row{display:flex;align-items:stretch;gap:0;margin-bottom:1.3rem;background:var(--accent-ll);border-radius:var(--r);border:1px solid #c0d4f8;overflow:hidden}
.m-price-main{padding:.9rem 1.2rem;flex:1}
.m-price-big{font-family:'Lora',serif;font-size:1.85rem;font-weight:700;color:var(--accent);line-height:1}
.m-price-big small{font-family:'Plus Jakarta Sans',sans-serif;font-size:.72rem;color:var(--muted);font-weight:400}
.m-price-sub{padding:.9rem 1rem;border-left:1px solid #c0d4f8;display:flex;flex-direction:column;justify-content:center}
.m-price-sub span{font-size:.67rem;color:var(--muted);text-transform:uppercase;letter-spacing:.05em;font-weight:600}
.m-price-sub strong{font-size:.9rem;font-weight:700;color:var(--text);margin-top:2px}
.m-desc{color:var(--muted);font-size:.86rem;line-height:1.78;margin-bottom:1.3rem;padding-bottom:1.3rem;border-bottom:1px solid var(--border)}
.m-grid{display:grid;grid-template-columns:1fr 1fr 1fr;gap:.7rem;margin-bottom:1.3rem}
.mf{background:var(--warm);border-radius:8px;padding:.65rem .82rem;border:1px solid var(--border)}
.mf label{font-size:.64rem;color:var(--muted);text-transform:uppercase;letter-spacing:.07em;font-weight:700;display:block;margin-bottom:.18rem}
.mf value{font-weight:700;font-size:.84rem;color:var(--text)}
.m-tags{display:flex;flex-wrap:wrap;gap:5px;margin-bottom:1.4rem}
.m-actions{display:flex;gap:.7rem}
.btn-call{flex:1;background:var(--accent);color:#fff;border:none;padding:.76rem;border-radius:9px;font-family:'Plus Jakarta Sans',sans-serif;font-weight:700;font-size:.9rem;cursor:pointer;transition:background .18s}
.btn-call:hover{background:#1240a8}
.btn-wa{background:#25D366;color:#fff;border:none;padding:.76rem 1.2rem;border-radius:9px;font-family:'Plus Jakarta Sans',sans-serif;font-size:.86rem;font-weight:600;cursor:pointer;transition:background .18s}
.btn-wa:hover{background:#1db954}
.btn-share{background:var(--warm);border:1.5px solid var(--border);color:var(--muted);padding:.76rem 1rem;border-radius:9px;cursor:pointer;font-size:.95rem;transition:all .18s}
.btn-share:hover{border-color:var(--accent);color:var(--accent)}

/* PUB MODAL */
.pub-prog{display:flex;gap:.4rem;margin-bottom:1.4rem}
.pd{flex:1;height:4px;border-radius:2px;background:var(--border);transition:background .3s}
.pd.on{background:var(--accent)}
.ps{display:none}.ps.active{display:block}
.fr{display:grid;gap:.8rem;margin-bottom:.8rem}
.fr2{grid-template-columns:1fr 1fr}
.fgr{display:flex;flex-direction:column;gap:.28rem}
.fgr label{font-size:.68rem;color:var(--muted);font-weight:700;text-transform:uppercase;letter-spacing:.06em}
.fgr input,.fgr select,.fgr textarea{background:var(--warm);border:1.5px solid var(--border);color:var(--text);padding:.55rem .82rem;border-radius:8px;font-family:'Plus Jakarta Sans',sans-serif;font-size:.86rem;font-weight:500;outline:none;transition:border .2s;-webkit-appearance:none}
.fgr input:focus,.fgr select:focus,.fgr textarea:focus{border-color:var(--accent);background:#fff}
.fgr textarea{resize:vertical;min-height:76px}
.pub-nav{display:flex;justify-content:space-between;align-items:center;margin-top:1.1rem}
.btn-next{background:var(--accent);color:#fff;border:none;padding:.62rem 1.4rem;border-radius:8px;font-family:'Plus Jakarta Sans',sans-serif;font-weight:700;font-size:.86rem;cursor:pointer;transition:background .18s}
.btn-next:hover{background:#1240a8}
.btn-back{background:none;border:none;color:var(--muted);font-size:.83rem;font-weight:600;cursor:pointer;padding:.62rem .9rem}
.btn-back:hover{color:var(--text)}

@keyframes fadeUp{from{opacity:0;transform:translateY(14px)}to{opacity:1;transform:translateY(0)}}
.card{animation:fadeUp .32s ease both}
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <a class="logo" href="#"><em>TUCADI</em></a>
  <div class="nav-links">
    <a href="#">Locales</a><a href="#">Zonas</a><a href="#">Cómo funciona</a><a href="#">Blog</a><a href="#">Contacto</a>
  </div>
  <div class="nav-actions">
    <button class="btn-out">Iniciar sesión</button>
    <button class="btn-prim" onclick="openPub()">+ Publicar local</button>
  </div>
</nav>

<!-- HERO -->
<div class="hero">
  <div class="hero-inner">
    <div>
      <div class="hero-eyebrow">Hermosillo · Renta de Locales</div>
      <h1>Encuentra el local comercial<br><i>ideal</i> para tu negocio</h1>
      <p class="hero-sub">Directorio actualizado de locales en renta en Hermosillo. Sin intermediarios, sin comisiones. Conectamos directamente con propietarios.</p>
      <div class="hero-search">
        <input id="txt-q" type="text" placeholder="🔍  Buscar por colonia, calle o tipo…" oninput="filtrar()">
        <button class="btn-sh" onclick="filtrar()">Buscar</button>
      </div>
      <div class="chips">
        <span class="chip on" onclick="chipClick(this,'')">Todos</span>
        <span class="chip" onclick="chipClick(this,'Local en plaza')">🏬 Plazas</span>
        <span class="chip" onclick="chipClick(this,'Local en avenida')">🛣️ Avenidas</span>
        <span class="chip" onclick="chipClick(this,'Bodega')">📦 Bodegas</span>
        <span class="chip" onclick="chipClick(this,'Oficina')">💼 Oficinas</span>
        <span class="chip" onclick="chipClick(this,'Restaurante')">🍴 Restaurantes</span>
      </div>
    </div>
    <div class="hero-illo">
      <svg viewBox="0 0 400 290" xmlns="http://www.w3.org/2000/svg" fill="none">
        <rect width="400" height="290" fill="#f0f7f4"/>
        <circle cx="340" cy="52" r="30" fill="#fde68a" opacity=".6"/>
        <rect x="8" y="105" width="52" height="185" fill="#c8d8d4" rx="4"/>
        <rect x="18" y="85" width="32" height="22" fill="#b8ccc8" rx="2"/>
        <rect x="65" y="125" width="42" height="165" fill="#b8d4cc" rx="4"/>
        <rect x="112" y="92" width="58" height="198" fill="#a8ccc4" rx="4"/>
        <rect x="182" y="68" width="88" height="222" fill="#d4e8e2" rx="6"/>
        <rect x="192" y="53" width="68" height="18" fill="#c4d8d2" rx="3"/>
        <rect x="195" y="83" width="17" height="17" fill="#9ec8bc" rx="2"/>
        <rect x="218" y="83" width="17" height="17" fill="#9ec8bc" rx="2"/>
        <rect x="241" y="83" width="17" height="17" fill="#fde68a" opacity=".8" rx="2"/>
        <rect x="195" y="108" width="17" height="17" fill="#9ec8bc" rx="2"/>
        <rect x="218" y="108" width="17" height="17" fill="#fde68a" opacity=".8" rx="2"/>
        <rect x="241" y="108" width="17" height="17" fill="#9ec8bc" rx="2"/>
        <rect x="195" y="133" width="17" height="17" fill="#fde68a" opacity=".8" rx="2"/>
        <rect x="218" y="133" width="17" height="17" fill="#9ec8bc" rx="2"/>
        <rect x="241" y="133" width="17" height="17" fill="#9ec8bc" rx="2"/>
        <rect x="211" y="242" width="30" height="48" fill="#4a80e0" rx="3"/>
        <circle cx="236" cy="268" r="2.3" fill="#1a4fc4"/>
        <rect x="275" y="115" width="62" height="175" fill="#cce0da" rx="4"/>
        <rect x="335" y="132" width="48" height="158" fill="#bcd4cc" rx="4"/>
        <rect x="288" y="130" width="13" height="13" fill="#90b8ac" rx="2"/>
        <rect x="307" y="130" width="13" height="13" fill="#fde68a" opacity=".7" rx="2"/>
        <rect x="288" y="150" width="13" height="13" fill="#fde68a" opacity=".7" rx="2"/>
        <rect x="307" y="150" width="13" height="13" fill="#90b8ac" rx="2"/>
        <rect x="190" y="173" width="72" height="21" fill="#1a4fc4" rx="4"/>
        <text x="226" y="187" font-size="8" fill="#fff" text-anchor="middle" font-family="serif" font-weight="700">TUCADI</text>
        <rect x="0" y="268" width="400" height="22" fill="#c8c0b0"/>
        <rect x="0" y="260" width="400" height="10" fill="#d8d0c0"/>
        <rect x="45" y="273" width="28" height="3" fill="rgba(255,255,255,.4)" rx="1"/>
        <rect x="105" y="273" width="28" height="3" fill="rgba(255,255,255,.4)" rx="1"/>
        <rect x="195" y="273" width="28" height="3" fill="rgba(255,255,255,.4)" rx="1"/>
        <rect x="275" y="273" width="28" height="3" fill="rgba(255,255,255,.4)" rx="1"/>
        <rect x="155" y="228" width="5" height="36" fill="#6080c0"/>
        <circle cx="158" cy="214" r="20" fill="#6090d8" opacity=".7"/>
        <rect x="273" y="232" width="5" height="32" fill="#6080c0"/>
        <circle cx="276" cy="218" r="18" fill="#6090d8" opacity=".65"/>
        <circle cx="226" cy="36" r="11" fill="#1a4fc4"/>
        <circle cx="226" cy="36" r="5" fill="#fff"/>
        <line x1="226" y1="47" x2="226" y2="54" stroke="#1a4fc4" stroke-width="2"/>
      </svg>
    </div>
  </div>
  <div class="hero-stats">
    <div class="hst"><div class="hst-n" id="cnt-n">8</div><div class="hst-l">Locales activos</div></div>
    <div class="hst"><div class="hst-n">12</div><div class="hst-l">Colonias</div></div>
    <div class="hst"><div class="hst-n">$7.5K</div><div class="hst-l">Renta mínima</div></div>
    <div class="hst"><div class="hst-n">Gratis</div><div class="hst-l">Publicar</div></div>
    <div class="hst"><div class="hst-n">24h</div><div class="hst-l">Respuesta</div></div>
  </div>
</div>

<!-- FILTROS -->
<div class="fw">
  <div class="fc">
    <div class="fg"><label>Zona / Colonia</label>
      <select id="f-zona" onchange="filtrar()">
        <option value="">Todas las zonas</option>
        <option>Centro</option><option>Pitic</option><option>Villa de Seris</option>
        <option>Bugambilias</option><option>Villa Satélite</option><option>Perisur</option><option>San Benito</option>
      </select>
    </div>
    <div class="fg"><label>Tipo de local</label>
      <select id="f-tipo" onchange="filtrar()">
        <option value="">Todos los tipos</option>
        <option>Local en plaza</option><option>Local en avenida</option>
        <option>Bodega</option><option>Oficina</option><option>Restaurante</option>
      </select>
    </div>
    <div class="fg"><label>Renta máx. ($/mes)</label>
      <select id="f-precio" onchange="filtrar()">
        <option value="">Sin límite</option>
        <option value="10000">Hasta $10,000</option><option value="20000">Hasta $20,000</option>
        <option value="35000">Hasta $35,000</option><option value="50000">Hasta $50,000</option>
      </select>
    </div>
    <div class="fg"><label>Superficie mín.</label>
      <select id="f-m2" onchange="filtrar()">
        <option value="">Cualquier tamaño</option>
        <option value="20">20 m²+</option><option value="50">50 m²+</option>
        <option value="100">100 m²+</option><option value="200">200 m²+</option>
      </select>
    </div>
    <div class="fg"><label>Estacionamiento</label>
      <select id="f-est" onchange="filtrar()">
        <option value="">Indiferente</option><option value="si">Con estacionamiento</option>
      </select>
    </div>
    <button class="btn-fil" onclick="filtrar()">Filtrar</button>
    <button class="btn-cl" onclick="resetF()">↺ Limpiar</button>
  </div>
</div>

<!-- GRID -->
<div class="sec">
  <div class="sec-head">
    <span class="sec-title">Locales disponibles</span>
    <div style="display:flex;align-items:center;gap:.8rem;flex-wrap:wrap">
      <span class="pill" id="pill-cnt">8 locales</span>
      <div class="sort-row">
        <span class="sort-lbl">Ordenar:</span>
        <button class="sb on" onclick="sortBy('rel',this)">Relevancia</button>
        <button class="sb" onclick="sortBy('pa',this)">Precio ↑</button>
        <button class="sb" onclick="sortBy('pd',this)">Precio ↓</button>
        <button class="sb" onclick="sortBy('m2',this)">Mayor m²</button>
      </div>
    </div>
  </div>
  <div class="grid" id="grid"></div>
</div>

<!-- HOW -->
<div class="how">
  <div class="how-in">
    <h2>¿Cómo funciona TUCADI?</h2>
    <p class="how-sub">Encontrar o publicar tu local es rápido, gratis y sin complicaciones.</p>
    <div class="how-steps">
      <div class="step"><span class="step-ico">🔍</span><div class="step-n">1</div><h3>Busca y filtra</h3><p>Usa los filtros por zona, tipo y precio para encontrar exactamente lo que necesitas.</p></div>
      <div class="step"><span class="step-ico">📋</span><div class="step-n">2</div><h3>Revisa detalles</h3><p>Consulta superficie, características, servicios incluidos y precio por m² de cada local.</p></div>
      <div class="step"><span class="step-ico">📱</span><div class="step-n">3</div><h3>Contacta directo</h3><p>Habla con el propietario por teléfono o WhatsApp. Sin intermediarios ni comisiones.</p></div>
      <div class="step"><span class="step-ico">🤝</span><div class="step-n">4</div><h3>Cierra el trato</h3><p>Visita el local, negocia condiciones y firma tu contrato. Así de sencillo.</p></div>
    </div>
  </div>
</div>

<!-- ZONAS -->
<div class="zonas">
  <div class="zonas-in">
    <div class="sec-title" style="font-size:1.22rem;font-family:'Lora',serif;font-weight:700">Explorar por zona</div>
    <div class="zonas-grid" id="zonas-grid"></div>
  </div>
</div>

<!-- TESTIMONIOS -->
<div class="testi">
  <h2>Lo que dicen nuestros usuarios</h2>
  <p class="testi-sub">Propietarios y empresarios que ya usan TUCADI en Hermosillo</p>
  <div class="tgrid">
    <div class="tc"><div class="tc-stars">★★★★★</div><p class="tc-text">"Publiqué mi local y en menos de una semana ya tenía tres interesados. El proceso es sencillo y no cobran nada."</p><div class="tc-auth"><div class="tc-av" style="background:#e8f2ef;color:#1a4fc4">MR</div><div class="tc-info"><strong>Miguel R.</strong><small>Propietario · Centro</small></div></div></div>
    <div class="tc"><div class="tc-stars">★★★★★</div><p class="tc-text">"Encontré el local perfecto para mi cafetería en Bugambilias. Contacté directo al dueño, sin pagar comisión a ninguna inmobiliaria."</p><div class="tc-auth"><div class="tc-av" style="background:#fdf0e4;color:#b86a2a">AL</div><div class="tc-info"><strong>Ana L.</strong><small>Emprendedora · Bugambilias</small></div></div></div>
    <div class="tc"><div class="tc-stars">★★★★☆</div><p class="tc-text">"Los filtros son muy útiles. Puse exactamente el tamaño y precio que buscaba y encontré varias opciones de inmediato."</p><div class="tc-auth"><div class="tc-av" style="background:#e8eef8;color:#3060a8">JV</div><div class="tc-info"><strong>Jorge V.</strong><small>Comerciante · Pitic</small></div></div></div>
  </div>
</div>

<!-- CTA -->
<div class="cta-w">
  <div class="cta-box">
    <div class="cta-txt">
      <h2>¿Tienes un local disponible para rentar?</h2>
      <p>Publica gratis en minutos y llega a cientos de emprendedores que buscan local en Hermosillo ahora mismo.</p>
    </div>
    <button class="btn-cta" onclick="openPub()">Publicar mi local gratis →</button>
  </div>
</div>

<!-- FOOTER -->
<footer>
  <div class="ft-in">
    <div class="ft-top">
      <div class="ft-brand">
        <a class="logo" href="#"><em>TUCADI</em></a>
        <p>El directorio más completo de locales comerciales en renta en Hermosillo, Sonora. Sin intermediarios.</p>
      </div>
      <div class="ft-col"><h4>Locales</h4><a href="#">Ver todos</a><a href="#">En avenidas</a><a href="#">En plazas</a><a href="#">Bodegas</a><a href="#">Oficinas</a></div>
      <div class="ft-col"><h4>Zonas</h4><a href="#">Centro</a><a href="#">Bugambilias</a><a href="#">Pitic</a><a href="#">San Benito</a><a href="#">Perisur</a></div>
      <div class="ft-col"><h4>TUCADI</h4><a href="#">Cómo funciona</a><a href="#">Publicar local</a><a href="#">Blog</a><a href="#">Contacto</a><a href="#">Privacidad</a></div>
    </div>
    <div class="ft-bot"><p>© 2025 TUCADI · Hecho con ❤️ en Sonora, México</p><span class="ft-bdg">Directorio gratuito</span></div>
  </div>
</footer>

<!-- MODAL DETALLE -->
<div class="ov" id="ov-d" onclick="closeD(event)">
  <div class="modal">
    <div class="m-thumb" id="m-thumb">
      <button class="m-close" onclick="closeD()">✕</button>
    </div>
    <div class="m-body">
      <div class="m-zona" id="m-zona"></div>
      <div class="m-name" id="m-name"></div>
      <div class="m-rating"><span class="m-stars" id="m-stars"></span>&nbsp;<span id="m-rat-n"></span>&nbsp;·&nbsp;<span id="m-views"></span></div>
      <div class="m-price-row">
        <div class="m-price-main">
          <div class="m-price-big" id="m-price"></div>
          <div style="font-size:.68rem;color:var(--muted);margin-top:3px">renta mensual</div>
        </div>
        <div class="m-price-sub"><span>Por m²</span><strong id="m-pm2"></strong></div>
        <div class="m-price-sub"><span>Depósito</span><strong id="m-dep"></strong></div>
      </div>
      <p class="m-desc" id="m-desc"></p>
      <div class="m-grid">
        <div class="mf"><label>Superficie</label><value id="m-m2"></value></div>
        <div class="mf"><label>Tipo</label><value id="m-tipo"></value></div>
        <div class="mf"><label>Estac.</label><value id="m-est"></value></div>
        <div class="mf"><label>Servicios</label><value id="m-serv"></value></div>
        <div class="mf"><label>Disponible</label><value id="m-disp"></value></div>
        <div class="mf"><label>Antigüedad</label><value id="m-age"></value></div>
      </div>
      <div class="m-tags" id="m-tags"></div>
      <div class="m-actions">
        <button class="btn-call" id="m-tel">📞 Llamar al propietario</button>
        <button class="btn-wa" id="m-wa">💬 WhatsApp</button>
        <button class="btn-share" onclick="alert('¡Liga copiada!')">🔗</button>
      </div>
    </div>
  </div>
</div>

<!-- MODAL PUBLICAR -->
<div class="ov" id="ov-p" onclick="closePub(event)">
  <div class="modal" style="max-width:540px">
    <div class="m-body">
      <div style="display:flex;justify-content:space-between;align-items:center;margin-bottom:1.1rem">
        <span style="font-family:'Lora',serif;font-size:1.25rem;font-weight:700">Publicar mi local</span>
        <button class="m-close" style="position:static;width:28px;height:28px" onclick="closePub()">✕</button>
      </div>
      <div class="pub-prog"><div class="pd on" id="pd1"></div><div class="pd" id="pd2"></div><div class="pd" id="pd3"></div></div>

      <div class="ps active" id="ps1">
        <p style="color:var(--muted);font-size:.82rem;margin-bottom:1.1rem">Paso 1 de 3 — Información básica</p>
        <div class="fr"><div class="fgr"><label>Nombre del local o dirección</label><input type="text" placeholder="Ej. Local en Blvd. Solidaridad esq. Reforma"></div></div>
        <div class="fr fr2">
          <div class="fgr"><label>Zona / Colonia</label><select><option>Centro</option><option>Pitic</option><option>Bugambilias</option><option>Villa Satélite</option><option>San Benito</option><option>Perisur</option><option>Villa de Seris</option></select></div>
          <div class="fgr"><label>Tipo de local</label><select><option>Local en avenida</option><option>Local en plaza</option><option>Bodega</option><option>Oficina</option><option>Restaurante</option></select></div>
        </div>
        <div class="fr fr2">
          <div class="fgr"><label>Renta mensual ($)</label><input type="number" placeholder="18,000"></div>
          <div class="fgr"><label>Superficie (m²)</label><input type="number" placeholder="60"></div>
        </div>
        <div class="pub-nav"><span></span><button class="btn-next" onclick="pubStep(2)">Siguiente →</button></div>
      </div>

      <div class="ps" id="ps2">
        <p style="color:var(--muted);font-size:.82rem;margin-bottom:1.1rem">Paso 2 de 3 — Detalles del local</p>
        <div class="fr fr2">
          <div class="fgr"><label>Depósito requerido</label><input type="text" placeholder="1 mes / 2 meses…"></div>
          <div class="fgr"><label>Estacionamiento</label><select><option>Sí, incluido</option><option>No incluido</option><option>En calle</option><option>En plaza</option></select></div>
        </div>
        <div class="fr fr2">
          <div class="fgr"><label>Servicios incluidos</label><input type="text" placeholder="Agua, luz, internet…"></div>
          <div class="fgr"><label>Disponibilidad</label><input type="text" placeholder="Inmediata / 1 mes…"></div>
        </div>
        <div class="fr"><div class="fgr"><label>Descripción del local</label><textarea placeholder="Describe el local: ubicación, características especiales, giro recomendado, estado del inmueble…"></textarea></div></div>
        <div class="pub-nav"><button class="btn-back" onclick="pubStep(1)">← Atrás</button><button class="btn-next" onclick="pubStep(3)">Siguiente →</button></div>
      </div>

      <div class="ps" id="ps3">
        <p style="color:var(--muted);font-size:.82rem;margin-bottom:1.1rem">Paso 3 de 3 — Datos de contacto</p>
        <div class="fr"><div class="fgr"><label>Tu nombre completo</label><input type="text" placeholder="Nombre del propietario o encargado"></div></div>
        <div class="fr fr2">
          <div class="fgr"><label>Teléfono (WhatsApp)</label><input type="tel" placeholder="662 XXX XXXX"></div>
          <div class="fgr"><label>Correo electrónico</label><input type="email" placeholder="correo@ejemplo.com"></div>
        </div>
        <div class="fr"><div class="fgr"><label>Preferencia de contacto</label><select><option>WhatsApp y llamadas</option><option>Solo WhatsApp</option><option>Solo correo</option><option>Cualquier medio</option></select></div></div>
        <div style="background:var(--accent-ll);border:1px solid #b8d0f8;border-radius:8px;padding:.82rem 1rem;margin:.5rem 0;font-size:.8rem;color:var(--muted)">
          ✅ Tu local será revisado y publicado en menos de 24 horas. El servicio es completamente gratuito.
        </div>
        <div class="pub-nav"><button class="btn-back" onclick="pubStep(2)">← Atrás</button><button class="btn-next" onclick="submitPub()">Publicar gratis ✓</button></div>
      </div>
    </div>
  </div>
</div>

<script>
const DB = [
  {id:1,name:"Local en Blvd. Solidaridad",zona:"Centro",tipo:"Local en avenida",m2:85,precio:22000,dep:"1 mes",badge:"hot",rat:4.7,views:43,tags:[{t:"Alta afluencia",c:"tg"},{t:"Esquina",c:"to"},{t:"2 baños",c:"tb"},{t:"Remodelado 2023",c:"tp"}],est:"Sí, 4 lugares",serv:"Agua, luz, internet",disp:"Inmediata",age:"8 años",tel:"662 100 2200",desc:"Excelente ubicación sobre Blvd. Solidaridad con alto flujo vehicular y peatonal. Ideal para restaurante, tienda o clínica. Cuenta con fachada amplia de 7m, espacio trasero para almacén de 15m² y dos baños. Recientemente remodelado con acabados modernos.",p:["#d0e8e0","#9eceba"]},
  {id:2,name:"Oficina en Plaza San Benito",zona:"San Benito",tipo:"Local en plaza",m2:45,precio:12500,dep:"2 meses",badge:"new",rat:4.4,views:28,tags:[{t:"Plaza establecida",c:"tg"},{t:"A/C central",c:"tb"},{t:"Planta baja",c:"tx"},{t:"Servicios incluidos",c:"to"}],est:"Plaza (incluido)",serv:"Agua y luz incluidos",disp:"Inmediata",age:"5 años",tel:"662 200 1133",desc:"Oficina o local comercial dentro de plaza con muy buena afluencia. Perfecto para consultorio, estética, tienda de ropa o servicios. Incluye servicios básicos en la renta y acceso a baños comunes de la plaza.",p:["#fce8d0","#f0c48a"]},
  {id:3,name:"Bodega industrial Periférico",zona:"Perisur",tipo:"Bodega",m2:320,precio:48000,dep:"2 meses",badge:"ok",rat:4.2,views:19,tags:[{t:"Acceso trailer",c:"to"},{t:"Portón eléctrico",c:"tb"},{t:"Piso nivelado",c:"tx"},{t:"Vigilancia 24h",c:"tg"}],est:"Patio privado",serv:"3 fases eléct., agua",disp:"15 días",age:"12 años",tel:"662 300 4455",desc:"Bodega de gran capacidad con acceso para vehículos de carga, altura libre de 6m y piso de concreto nivelado. Ideal para distribuidoras, manufactura o logística. Portón automatizado, oficina integrada y vigilancia privada 24 horas.",p:["#dce8f0","#b0c8dc"]},
  {id:4,name:"Local en Bugambilias Centro",zona:"Bugambilias",tipo:"Local en avenida",m2:60,precio:16000,dep:"1 mes",badge:"new",rat:4.5,views:35,tags:[{t:"Zona residencial",c:"tg"},{t:"Vitrina amplia",c:"tb"},{t:"A/C",c:"to"}],est:"Calle (no incluido)",serv:"Agua y luz",disp:"Inmediata",age:"4 años",tel:"662 150 9900",desc:"Perfecto para tienda de abarrotes, papelería, estética o negocios de servicio. Zona residencial con alta demanda. Vitrina amplia de 5.5m hacia la calle y acabados modernos. Se entrega pintado.",p:["#ead4e8","#cca0c8"]},
  {id:5,name:"Restaurante equipado Centro",zona:"Centro",tipo:"Restaurante",m2:110,precio:35000,dep:"2 meses",badge:"hot",rat:4.8,views:62,tags:[{t:"Cocina equipada",c:"to"},{t:"Campana industrial",c:"tg"},{t:"Capacidad 40 pax",c:"tb"},{t:"Trampa grasa",c:"tx"}],est:"Sí, 8 lugares",serv:"Gas, agua, luz",disp:"Inmediata",age:"6 años",tel:"662 400 7788",desc:"Local ya adaptado para restaurante o cafetería con cocina equipada: estufa industrial 8 quemadores, refrigerador, campana de ventilación y trampa de grasa. Salón con capacidad para 40 comensales. Listo para operar el primer día.",p:["#fce0c8","#f4a870"]},
  {id:6,name:"Módulo en Plaza Satélite",zona:"Villa Satélite",tipo:"Local en plaza",m2:22,precio:7500,dep:"1 mes",badge:"ok",rat:4.0,views:17,tags:[{t:"Bajo costo",c:"tg"},{t:"Plaza techada",c:"tb"},{t:"Alta circulación",c:"tx"}],est:"Plaza",serv:"Incluidos",disp:"Inmediata",age:"3 años",tel:"662 500 1122",desc:"Módulo pequeño dentro de plaza con alta circulación diaria. Ideal para negocio unipersonal: accesorios, dulcería, servicios express o comida rápida. Servicios incluidos en la renta. Excelente opción para comenzar.",p:["#d0e8d8","#98c8a8"]},
  {id:7,name:"Local Pitic con mezzanine",zona:"Pitic",tipo:"Local en avenida",m2:95,precio:19500,dep:"1 mes",badge:"new",rat:4.3,views:24,tags:[{t:"Mezzanine",c:"tp"},{t:"Doble altura",c:"tb"},{t:"Fachada renovada",c:"to"}],est:"2 lugares al frente",serv:"Agua y luz",disp:"1 mes",age:"10 años",tel:"662 600 3344",desc:"Local de doble altura con mezzanine aprovechable como oficina, almacén o área de trabajo adicional (+25m²). Colonia activa con mucho comercio local. Fachada recientemente renovada, instalaciones eléctricas en buen estado.",p:["#e8f0d0","#c0d890"]},
  {id:8,name:"Nave semi-industrial Seris",zona:"Villa de Seris",tipo:"Bodega",m2:180,precio:27000,dep:"2 meses",badge:"ok",rat:4.1,views:21,tags:[{t:"Nave industrial",c:"to"},{t:"Altura 5.5m",c:"tb"},{t:"Ventilación natural",c:"tg"},{t:"Rampa de acceso",c:"tx"}],est:"Patio amplio",serv:"3 fases disponible",disp:"Disponible ya",age:"15 años",tel:"662 700 5566",desc:"Nave semi-industrial en zona estratégica cerca de Blvd. Solidaridad. Altura libre de 5.5m con ventilación cruzada natural. Rampa de acceso, patio para maniobras y conexión a 3 fases disponible. Ideal para taller, manufactura o logística.",p:["#dce8f0","#b0c8e0"]},
];

const ZONAS=[{n:"Centro",c:2,i:"🏛️"},{n:"Bugambilias",c:1,i:"🌸"},{n:"Pitic",c:1,i:"🌵"},{n:"San Benito",c:1,i:"🏬"},{n:"Villa Satélite",c:1,i:"🛸"},{n:"Perisur",c:1,i:"🏭"},{n:"Villa de Seris",c:1,i:"🔧"}];

let favs=new Set(), sortM='rel', chipT='';

function starsStr(r){let s='';for(let i=1;i<=5;i++)s+=i<=Math.round(r)?'★':'☆';return s;}

function thumb(l){
  return `<svg viewBox="0 0 400 178" xmlns="http://www.w3.org/2000/svg">
    <rect width="400" height="178" fill="${l.p[0]}"/>
    <circle cx="320" cy="38" r="78" fill="${l.p[1]}" opacity=".4"/>
    <circle cx="48" cy="145" r="52" fill="${l.p[1]}" opacity=".28"/>
    <rect x="0" y="138" width="400" height="40" fill="${l.p[1]}" opacity=".13"/>
    <text x="200" y="85" font-size="14" fill="${l.p[1]}" fill-opacity=".95" text-anchor="middle" font-family="serif" font-weight="700">${l.m2} m²</text>
    <text x="200" y="106" font-size="10" fill="${l.p[1]}" fill-opacity=".75" text-anchor="middle" font-family="sans-serif">${l.tipo}</text>
    <text x="200" y="126" font-size="11" fill="${l.p[1]}" fill-opacity=".65" text-anchor="middle" font-family="sans-serif" font-weight="600">📍 ${l.zona}</text>
  </svg>`;
}

function bdg(b){return b==='new'?'<span class="bdg bdg-new">Nuevo</span>':b==='hot'?'<span class="bdg bdg-hot">🔥 Popular</span>':'<span class="bdg bdg-ok">✓ Disponible</span>';}

function renderCards(list){
  const g=document.getElementById('grid');
  if(!list.length){g.innerHTML='<p style="grid-column:1/-1;color:var(--muted);padding:2rem 0;font-size:.93rem">No encontramos locales con esos filtros. Prueba ampliando la búsqueda.</p>';return;}
  g.innerHTML=list.map((l,i)=>`
  <div class="card" style="animation-delay:${i*.06}s" onclick="openD(${l.id})">
    <div class="cthumb">
      ${thumb(l)}
      <div class="cthumb-ov"></div>
      ${bdg(l.badge)}
      <div class="cfav ${favs.has(l.id)?'on':''}" onclick="toggleF(event,${l.id})">${favs.has(l.id)?'❤️':'🤍'}</div>
      <div class="cviews">👁 ${l.views} visitas</div>
    </div>
    <div class="cbody">
      <div class="ctop">
        <div class="czona">📍 ${l.zona}</div>
        <div class="crat">${starsStr(l.rat)} ${l.rat}</div>
      </div>
      <div class="cname">${l.name}</div>
      <div class="ctags">
        ${l.tags.slice(0,3).map(t=>`<span class="tag ${t.c}">${t.t}</span>`).join('')}
        <span class="tag tx">${l.tipo}</span>
      </div>
      <div class="cspecs">
        <div class="cs">📐 Superficie: <span class="sv">&nbsp;${l.m2} m²</span></div>
        <div class="cs">🚗 Estac.: <span class="sv">&nbsp;${l.est.toLowerCase().includes('no')?'No':'Sí'}</span></div>
        <div class="cs">⚡ Servicios: <span class="sv">&nbsp;${l.serv.split(',')[0]}</span></div>
        <div class="cs">📅 Disp.: <span class="sv">&nbsp;${l.disp}</span></div>
      </div>
      <div class="cfoot">
        <div>
          <div class="cprice">$${l.precio.toLocaleString()} <small>/mes</small></div>
          <div class="cpm2">$${Math.round(l.precio/l.m2).toLocaleString()}/m²</div>
        </div>
        <button class="btn-ver">Ver detalles →</button>
      </div>
    </div>
  </div>`).join('');
  const n=list.length;
  document.getElementById('pill-cnt').textContent=`${n} local${n!==1?'es':''} encontrado${n!==1?'s':''}`;
  document.getElementById('cnt-n').textContent=DB.length;
}

function getF(){
  const zona=document.getElementById('f-zona').value;
  const tipo=document.getElementById('f-tipo').value||chipT;
  const precio=parseInt(document.getElementById('f-precio').value)||Infinity;
  const m2min=parseInt(document.getElementById('f-m2').value)||0;
  const est=document.getElementById('f-est').value;
  const q=(document.getElementById('txt-q').value||'').toLowerCase();
  return DB.filter(l=>
    (!zona||l.zona===zona)&&(!tipo||l.tipo===tipo)&&
    l.precio<=precio&&l.m2>=m2min&&
    (!est||est!=='si'||!l.est.toLowerCase().includes('no'))&&
    (!q||(l.name+l.zona+l.tipo+l.desc).toLowerCase().includes(q))
  );
}
function sortL(list){
  if(sortM==='pa')return[...list].sort((a,b)=>a.precio-b.precio);
  if(sortM==='pd')return[...list].sort((a,b)=>b.precio-a.precio);
  if(sortM==='m2')return[...list].sort((a,b)=>b.m2-a.m2);
  return list;
}
function filtrar(){renderCards(sortL(getF()));}
function sortBy(m,btn){sortM=m;document.querySelectorAll('.sb').forEach(b=>b.classList.remove('on'));btn.classList.add('on');filtrar();}
function chipClick(el,t){chipT=t;document.querySelectorAll('.chip').forEach(c=>c.classList.remove('on'));el.classList.add('on');filtrar();}
function resetF(){['f-zona','f-tipo','f-precio','f-m2','f-est'].forEach(id=>document.getElementById(id).value='');document.getElementById('txt-q').value='';chipT='';document.querySelectorAll('.chip').forEach(c=>c.classList.remove('on'));document.querySelector('.chip').classList.add('on');filtrar();}
function toggleF(e,id){e.stopPropagation();favs.has(id)?favs.delete(id):favs.add(id);filtrar();}

function openD(id){
  const l=DB.find(x=>x.id===id);if(!l)return;
  const th=document.getElementById('m-thumb');
  th.innerHTML=thumb(l)+'<button class="m-close" onclick="closeD()">✕</button>';
  th.style.cssText='height:195px;position:relative;border-radius:22px 22px 0 0;overflow:hidden';
  document.getElementById('m-zona').innerHTML='📍 '+l.zona;
  document.getElementById('m-name').textContent=l.name;
  document.getElementById('m-stars').textContent=starsStr(l.rat);
  document.getElementById('m-rat-n').textContent=l.rat+' ('+Math.floor(Math.random()*18+6)+' reseñas)';
  document.getElementById('m-views').textContent=l.views+' visitas esta semana';
  document.getElementById('m-price').innerHTML='$'+l.precio.toLocaleString()+' <small>/mes</small>';
  document.getElementById('m-pm2').textContent='$'+Math.round(l.precio/l.m2).toLocaleString()+'/m²';
  document.getElementById('m-dep').textContent=l.dep;
  document.getElementById('m-desc').textContent=l.desc;
  document.getElementById('m-m2').textContent=l.m2+' m²';
  document.getElementById('m-tipo').textContent=l.tipo;
  document.getElementById('m-est').textContent=l.est;
  document.getElementById('m-serv').textContent=l.serv;
  document.getElementById('m-disp').textContent=l.disp;
  document.getElementById('m-age').textContent=l.age;
  document.getElementById('m-tags').innerHTML=l.tags.map(t=>`<span class="tag ${t.c}">${t.t}</span>`).join('');
  document.getElementById('m-tel').onclick=()=>alert('Llamar al: '+l.tel);
  document.getElementById('m-wa').onclick=()=>window.open('https://wa.me/52'+l.tel.replace(/\D/g,'')+'?text=Hola, vi el local "'+l.name+'" en TUCADI y me interesa más información.','_blank');
  document.getElementById('ov-d').classList.add('open');
}
function closeD(e){if(!e||e.target===document.getElementById('ov-d'))document.getElementById('ov-d').classList.remove('open');}
function openPub(){document.getElementById('ov-p').classList.add('open');pubStep(1);}
function closePub(e){if(!e||e.target===document.getElementById('ov-p'))document.getElementById('ov-p').classList.remove('open');}
function pubStep(n){[1,2,3].forEach(i=>{document.getElementById('ps'+i).classList.toggle('active',i===n);document.getElementById('pd'+i).classList.toggle('on',i<=n);});}
function submitPub(){alert('¡Gracias! Tu local fue enviado para revisión.\nLo publicaremos en menos de 24 horas y te contactaremos para confirmar.');closePub();}

// Zonas
document.getElementById('zonas-grid').innerHTML=ZONAS.map(z=>`
  <div class="zchip" onclick="filterZona('${z.n}')">
    <div style="font-size:1.35rem;margin-bottom:.28rem">${z.i}</div>
    <div class="zchip-name">${z.n}</div>
    <div class="zchip-cnt">${z.c} local${z.c!==1?'es':''}</div>
  </div>`).join('');

function filterZona(z){document.getElementById('f-zona').value=z;document.querySelector('.sec').scrollIntoView({behavior:'smooth'});filtrar();}

// Init
filtrar();
</script>
</body>
</html>
