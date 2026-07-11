import { useState } from "react";

// ─── CONSTANTS ────────────────────────────────────────────────────────────────
const TUCADI_FEE_PCT = 0.10;
const PLATFORM_FEE_EVAL = 49; // siempre se cobra, independiente del precio del técnico
const RETENTION_DAYS = 7;
const fmt = (n) => `$${Number(n).toLocaleString("es-MX")} MXN`;

// ─── MOCK DATA ────────────────────────────────────────────────────────────────
const TECHNICIANS = [
  {
    id: 1, name: "Carlos Mendoza", rating: 4.9, reviewCount: 47, experienceYears: 12,
    services: ["Instalación", "Reparación", "Mantenimiento"],
    zone: "Centro / Pitic",
    description: "Técnico certificado con más de 12 años de experiencia en instalación y reparación de minisplits de todas las marcas. Trabajo garantizado, precios justos y atención el mismo día.",
    phone: "6621234567", avatar: "CM", avatarColor: "#1e3a5f",
    evaluationPrice: 150, evaluationModes: ["chat", "presencial"],
    jobs: [
      { id: "j1", name: "Instalación minisplit 1 ton", price: 1200, desc: "Incluye soporte, cañería 3m y conexión eléctrica." },
      { id: "j2", name: "Reparación / diagnóstico", price: 800, desc: "Revisión completa, carga de gas y reparación de fallas eléctricas." },
      { id: "j3", name: "Mantenimiento preventivo", price: 450, desc: "Lavado de filtros, revisión de compresor y verificación de refrigerante." },
    ],
  },
  {
    id: 2, name: "Roberto Salazar", rating: 4.8, reviewCount: 31, experienceYears: 8,
    services: ["Instalación", "Mantenimiento"],
    zone: "Villa del Real / Perisur",
    description: "Especialista en instalaciones residenciales y comerciales. Trabajo limpio, materiales de calidad y garantía de 6 meses en instalaciones nuevas.",
    phone: "6629876543", avatar: "RS", avatarColor: "#2d6a4f",
    evaluationPrice: 200, evaluationModes: ["presencial"],
    jobs: [
      { id: "j4", name: "Instalación completa con materiales", price: 1800, desc: "Minisplit hasta 2 ton, materiales incluidos, garantía 6 meses." },
      { id: "j5", name: "Mantenimiento preventivo", price: 500, desc: "Limpieza profunda, revisión eléctrica y reporte de condición." },
    ],
  },
  {
    id: 3, name: "Jesús Félix", rating: 4.7, reviewCount: 28, experienceYears: 6,
    services: ["Reparación", "Mantenimiento"],
    zone: "Lomas de Hermosillo / Bugambilias",
    description: "Me especializo en diagnóstico y reparación de equipos. Reviso fallas eléctricas, problemas de refrigerante y mantenimiento preventivo. Respondo rápido por WhatsApp.",
    phone: "6625551234", avatar: "JF", avatarColor: "#7b3f00",
    evaluationPrice: 100, evaluationModes: ["chat", "presencial"],
    jobs: [
      { id: "j6", name: "Reparación de compresor", price: 950, desc: "Diagnóstico y reparación de fallas en compresor y sistema de enfriamiento." },
      { id: "j7", name: "Mantenimiento básico", price: 350, desc: "Limpieza de filtros y revisión de niveles de refrigerante." },
    ],
  },
  {
    id: 4, name: "Miguel Valenzuela", rating: 4.6, reviewCount: 19, experienceYears: 4,
    services: ["Instalación", "Reparación"],
    zone: "San Benito / Proyecto Río",
    description: "Joven técnico con formación en refrigeración industrial. Trabajo con marcas LG, Samsung, Carrier y Daikin. Presupuesto sin costo.",
    phone: "6623334444", avatar: "MV", avatarColor: "#4a1942",
    evaluationPrice: 0, evaluationModes: ["chat", "presencial"],
    jobs: [
      { id: "j8", name: "Instalación estándar", price: 900, desc: "Instalación limpia con garantía de 3 meses en mano de obra." },
      { id: "j9", name: "Reparación general", price: 650, desc: "Diagnóstico y reparación de fallas comunes en minisplits." },
    ],
  },
];

const REVIEWS = {
  1: [
    { userName: "Ana G.", rating: 5, comment: "Excelente servicio, llegó puntual y dejó todo limpio. Lo recomiendo mucho." },
    { userName: "Luis R.", rating: 5, comment: "Resolvió el problema de mi minisplit en menos de una hora. Muy profesional." },
    { userName: "Patricia M.", rating: 4, comment: "Buen trabajo, precio justo. Solo tardó un poco más de lo esperado." },
    { userName: "Jorge A.", rating: 5, comment: "Ya es la tercera vez que lo contrato y siempre quedo satisfecho." },
  ],
  2: [
    { userName: "Sandra L.", rating: 5, comment: "Instaló dos equipos en mi casa, quedaron perfectos y muy ordenados los cables." },
    { userName: "Héctor N.", rating: 5, comment: "Muy responsable y puntual. Sabe lo que hace." },
    { userName: "Carmen V.", rating: 4, comment: "Buen precio y trabajo limpio. Lo volvería a contratar." },
  ],
  3: [
    { userName: "Ricardo P.", rating: 5, comment: "Diagnosticó el problema de mi equipo que otros no pudieron. 10/10." },
    { userName: "Mariana C.", rating: 4, comment: "Reparó mi split el mismo día que llamé. Muy eficiente." },
    { userName: "Eduardo S.", rating: 5, comment: "Sabe mucho de su trabajo, me explicó todo el proceso." },
  ],
  4: [
    { userName: "Fernanda O.", rating: 5, comment: "Joven muy profesional y honesto con los precios." },
    { userName: "Arturo M.", rating: 4, comment: "Instaló el equipo rápido y bien. Buena comunicación." },
  ],
};

// ─── GLOBAL STYLES ────────────────────────────────────────────────────────────
const G = `
  @import url('https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,400;9..144,600;9..144,700&family=DM+Sans:wght@300;400;500;600&display=swap');
  *,*::before,*::after{box-sizing:border-box;margin:0;padding:0}
  :root{
    --navy:#0f2540;--navy-mid:#1e3a5f;
    --amber:#d4860b;--amber-light:#f5a623;
    --wa:#25D366;--wa-dark:#1da851;
    --bg:#fafaf8;--bg-warm:#f5f3ef;
    --text:#1a1a1a;--mid:#4a4a4a;--muted:#888;--border:#e5e2db;
    --shadow:0 2px 12px rgba(15,37,64,0.07),0 1px 3px rgba(15,37,64,0.05);
    --shadow-lg:0 8px 32px rgba(15,37,64,0.13),0 2px 8px rgba(15,37,64,0.08);
    --r:12px;--rs:8px;
    --fd:'Fraunces',Georgia,serif;--fb:'DM Sans',system-ui,sans-serif;
    --green:#16a34a;--green-bg:#f0fdf4;
    --blue:#1d4ed8;--blue-bg:#eff6ff;
    --warn:#b45309;--warn-bg:#fffbeb;
  }
  html{scroll-behavior:smooth}
  body{font-family:var(--fb);background:var(--bg);color:var(--text);line-height:1.6;-webkit-font-smoothing:antialiased}
  a{color:inherit;text-decoration:none}
  button{font-family:var(--fb)}

  /* NAV */
  .nav{position:sticky;top:0;z-index:100;background:rgba(250,250,248,0.96);backdrop-filter:blur(12px);border-bottom:1px solid var(--border);padding:0 16px}
  .nav-in{max-width:1120px;margin:0 auto;display:flex;align-items:center;justify-content:space-between;height:56px}
  .logo{font-family:var(--fd);font-size:22px;font-weight:700;color:var(--navy);letter-spacing:-.5px;cursor:pointer;border:none;background:none}
  .logo span{color:var(--amber)}
  .nl{display:flex;gap:6px;align-items:center}
  .nlink{font-size:13px;font-weight:500;color:var(--mid);padding:7px 12px;border-radius:var(--rs);cursor:pointer;background:none;border:none;transition:all .15s}
  .nlink:hover{background:var(--bg-warm);color:var(--navy)}
  .ncta{font-size:13px;font-weight:600;color:var(--navy);padding:7px 14px;border-radius:var(--rs);cursor:pointer;background:none;border:1.5px solid var(--navy);transition:all .15s}
  .ncta:hover{background:var(--navy);color:white}
  @media(max-width:600px){.nl .nlink{display:none}}

  /* BUTTONS */
  .btn{display:inline-flex;align-items:center;gap:8px;font-family:var(--fb);font-weight:600;cursor:pointer;border:none;transition:all .18s;white-space:nowrap;border-radius:var(--rs)}
  .btn-navy{background:var(--navy);color:white;padding:13px 24px;font-size:15px}
  .btn-navy:hover{background:var(--navy-mid);transform:translateY(-1px);box-shadow:0 4px 16px rgba(15,37,64,.2)}
  .btn-amber{background:var(--amber);color:white;padding:13px 24px;font-size:15px}
  .btn-amber:hover{background:#b8730a;transform:translateY(-1px)}
  .btn-outline{background:white;color:var(--navy);padding:11px 18px;font-size:14px;border:1.5px solid var(--border)}
  .btn-outline:hover{border-color:var(--navy)}
  .btn-ghost{background:none;color:var(--mid);padding:8px 12px;font-size:14px;border:none}
  .btn-wa{background:var(--wa);color:white;padding:12px 20px;font-size:14px}
  .btn-wa:hover{background:var(--wa-dark);transform:translateY(-1px);box-shadow:0 4px 16px rgba(37,211,102,.3)}
  .btn-wa-lg{background:var(--wa);color:white;padding:14px 24px;font-size:15px;width:100%;justify-content:center}
  .btn-wa-lg:hover{background:var(--wa-dark)}
  .full{width:100%;justify-content:center}

  /* CARDS */
  .card{background:white;border-radius:var(--r);border:1px solid var(--border);box-shadow:var(--shadow);transition:box-shadow .2s,transform .2s}
  .card:hover{box-shadow:var(--shadow-lg);transform:translateY(-2px)}
  .card-flat{background:white;border-radius:var(--r);border:1px solid var(--border)}
  .card-hi{background:white;border-radius:var(--r);border:2px solid var(--navy);box-shadow:var(--shadow)}

  /* BADGES */
  .badge{display:inline-flex;align-items:center;gap:4px;font-size:12px;font-weight:600;padding:4px 10px;border-radius:20px;background:var(--bg-warm);color:var(--mid)}
  .b-navy{background:rgba(15,37,64,.08);color:var(--navy)}
  .b-amber{background:rgba(212,134,11,.1);color:var(--amber)}
  .b-green{background:var(--green-bg);color:var(--green)}
  .b-blue{background:var(--blue-bg);color:var(--blue)}

  /* LAYOUT */
  .sec{padding:64px 16px}.sec-sm{padding:36px 16px}
  .con{max-width:1120px;margin:0 auto}
  .divider{height:1px;background:var(--border);margin:20px 0}

  /* INPUTS */
  .inp{font-family:var(--fb);font-size:16px;padding:12px 16px;border-radius:var(--rs);border:1.5px solid var(--border);background:white;color:var(--text);width:100%;outline:none;transition:border-color .15s}
  .inp:focus{border-color:var(--navy)}
  .sel{font-family:var(--fb);font-size:16px;padding:12px 16px;border-radius:var(--rs);border:1.5px solid var(--border);background:white;color:var(--text);width:100%;cursor:pointer;outline:none;appearance:none;background-image:url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='12' height='8' viewBox='0 0 12 8'%3E%3Cpath d='M1 1l5 5 5-5' stroke='%23888' stroke-width='1.5' fill='none' stroke-linecap='round'/%3E%3C/svg%3E");background-repeat:no-repeat;background-position:right 14px center;padding-right:36px;transition:border-color .15s}
  .sel:focus{border-color:var(--navy)}
  .lbl{font-size:13px;font-weight:600;color:var(--mid);display:block;margin-bottom:6px}
  textarea.inp{resize:vertical;min-height:88px}

  /* ALERTS */
  .alert{border-radius:var(--rs);padding:13px 16px;font-size:13px;line-height:1.6}
  .al-info{background:var(--blue-bg);border:1px solid #bfdbfe;color:var(--blue)}
  .al-warn{background:var(--warn-bg);border:1px solid #fde68a;color:var(--warn)}
  .al-green{background:var(--green-bg);border:1px solid #bbf7d0;color:var(--green)}

  /* FEE BOX */
  .fbox{background:var(--bg-warm);border:1px solid var(--border);border-radius:var(--rs);padding:16px;font-size:13px}
  .fr{display:flex;justify-content:space-between;padding:5px 0;color:var(--mid)}
  .fr-total{font-weight:700;color:var(--navy);font-size:15px;border-top:1px solid var(--border);margin-top:6px;padding-top:10px;display:flex;justify-content:space-between}
  .fr-tech{color:var(--green);font-weight:600;display:flex;justify-content:space-between;padding:5px 0}

  /* AVATAR */
  .av{width:52px;height:52px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-family:var(--fd);font-weight:700;font-size:18px;color:white;flex-shrink:0}
  .av-lg{width:72px;height:72px;font-size:22px}

  /* SERVICE TAG */
  .stag{font-size:12px;font-weight:500;padding:4px 10px;border-radius:20px;background:var(--bg-warm);color:var(--mid);border:1px solid var(--border);display:inline-block}

  /* STEP TRACK */
  .strack{display:flex;align-items:center;margin-bottom:28px}
  .sdot{width:30px;height:30px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:12px;font-weight:700;flex-shrink:0}
  .sd-done{background:var(--navy);color:white}
  .sd-active{background:var(--amber);color:white}
  .sd-pending{background:var(--border);color:var(--muted)}
  .sline{flex:1;height:2px;background:var(--border)}
  .sl-done{background:var(--navy)}

  /* CHAT */
  .bubble{padding:10px 14px;border-radius:16px;font-size:14px;line-height:1.6;max-width:82%}
  .b-them{background:var(--bg-warm);border-radius:4px 16px 16px 16px;color:var(--text);align-self:flex-start}
  .b-me{background:var(--navy);color:white;border-radius:16px 4px 16px 16px;align-self:flex-end}

  /* ACTIVITY CARD */
  .acard{background:white;border-radius:var(--r);border:2px solid var(--amber);padding:20px}

  /* MODAL */
  .moverlay{position:fixed;inset:0;background:rgba(0,0,0,.45);z-index:300;display:flex;align-items:flex-end;justify-content:center}
  @media(min-width:600px){.moverlay{align-items:center;padding:24px}}
  .modal{background:white;border-radius:20px 20px 0 0;width:100%;max-width:500px;max-height:92vh;overflow-y:auto;padding:24px 20px 40px}
  @media(min-width:600px){.modal{border-radius:16px;padding:28px}}

  /* FOOTER */
  .foot{background:var(--navy);color:rgba(255,255,255,.7);padding:32px 16px}
  .foot-in{max-width:1120px;margin:0 auto;display:flex;justify-content:space-between;align-items:center;flex-wrap:wrap;gap:16px}
  .flogo{font-family:var(--fd);font-size:20px;font-weight:700;color:white}
  .flogo span{color:var(--amber-light)}

  /* MOBILE FLOAT BAR */
  .wafloat{display:none}
  @media(max-width:768px){
    .wafloat{display:flex;position:fixed;bottom:0;left:0;right:0;z-index:200;background:white;border-top:1px solid var(--border);padding:12px 16px;gap:10px;box-shadow:0 -4px 20px rgba(15,37,64,.1)}
    .has-wafloat{padding-bottom:78px}
    .hide-mobile{display:none!important}
  }
`;

// ─── ICONS ────────────────────────────────────────────────────────────────────
const WA = () => (
  <svg width="18" height="18" viewBox="0 0 24 24" fill="currentColor">
    <path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413z"/>
  </svg>
);

// ─── NAV ─────────────────────────────────────────────────────────────────────
function Nav({ nav }) {
  return (
    <nav className="nav">
      <div className="nav-in">
        <button className="logo" onClick={() => nav("home")}>TUCA<span>DI</span></button>
        <div className="nl">
          <button className="nlink" onClick={() => nav("list")}>Técnicos</button>
          <button className="nlink" onClick={() => nav("how")}>¿Cómo funciona?</button>
          <button className="ncta" onClick={() => nav("signup")}>Soy técnico</button>
        </div>
      </div>
    </nav>
  );
}

// ─── FOOTER ──────────────────────────────────────────────────────────────────
function Footer({ nav }) {
  return (
    <footer className="foot">
      <div className="foot-in">
        <div>
          <div className="flogo">TUCA<span>DI</span></div>
          <p style={{ fontSize: 13, marginTop: 6 }}>Técnicos locales de confianza · Hermosillo, Sonora</p>
        </div>
        <div style={{ display: "flex", gap: 4, flexWrap: "wrap" }}>
          {[["Inicio","home"],["Técnicos","list"],["¿Cómo funciona?","how"],["Registrarme","signup"]].map(([l,p]) => (
            <button key={p} className="btn btn-ghost" style={{ color: "rgba(255,255,255,.6)", fontSize: 13 }} onClick={() => nav(p)}>{l}</button>
          ))}
        </div>
        <p style={{ fontSize: 12, width: "100%", textAlign: "center", borderTop: "1px solid rgba(255,255,255,.1)", paddingTop: 16, marginTop: 4 }}>
          © 2025 TUCADI · Hermosillo, Sonora, México
        </p>
      </div>
    </footer>
  );
}

// ─── TECH CARD ────────────────────────────────────────────────────────────────
function TechCard({ tech, nav }) {
  const free = tech.evaluationPrice === 0;
  return (
    <div className="card" style={{ padding: 20 }}>
      <div style={{ display: "flex", gap: 14, alignItems: "flex-start", marginBottom: 14 }}>
        <div className="av" style={{ background: tech.avatarColor }}>{tech.avatar}</div>
        <div style={{ flex: 1, minWidth: 0 }}>
          <div style={{ display: "flex", alignItems: "flex-start", justifyContent: "space-between", gap: 6 }}>
            <h3 style={{ fontFamily: "var(--fd)", fontSize: 17, fontWeight: 600, color: "var(--navy)", lineHeight: 1.2 }}>{tech.name}</h3>
            <span className="badge b-amber" style={{ flexShrink: 0, fontSize: 11 }}>{tech.experienceYears} años</span>
          </div>
          <div style={{ display: "flex", alignItems: "center", gap: 6, marginTop: 4 }}>
            <span style={{ color: "var(--amber-light)", fontSize: 13 }}>{"★".repeat(Math.floor(tech.rating))}</span>
            <span style={{ fontWeight: 700, fontSize: 13, color: "var(--navy)" }}>{tech.rating}</span>
            <span style={{ fontSize: 12, color: "var(--muted)" }}>({tech.reviewCount})</span>
          </div>
          <div style={{ fontSize: 12, color: "var(--muted)", marginTop: 4 }}>📍 {tech.zone}</div>
        </div>
      </div>

      <div style={{ display: "flex", flexWrap: "wrap", gap: 6, marginBottom: 14 }}>
        {tech.services.map(s => <span key={s} className="stag">{s}</span>)}
      </div>

      {/* Eval price */}
      <div style={{ background: "var(--bg-warm)", borderRadius: "var(--rs)", padding: "10px 14px", marginBottom: 16, border: "1px solid var(--border)", display: "flex", justifyContent: "space-between", alignItems: "center" }}>
        <div>
          <div style={{ fontSize: 11, fontWeight: 600, color: "var(--muted)", textTransform: "uppercase", letterSpacing: ".5px" }}>Evaluación</div>
          <div style={{ fontSize: 15, fontWeight: 700, color: free ? "var(--green)" : "var(--navy)", marginTop: 2 }}>
            {free ? "Gratis" : fmt(tech.evaluationPrice)}
          </div>
          <div style={{ fontSize: 11, color: "var(--amber)", fontWeight: 600, marginTop: 2 }}>+ {fmt(PLATFORM_FEE_EVAL)} tarifa TUCADI</div>
        </div>
        <div style={{ display: "flex", gap: 5, flexWrap: "wrap", justifyContent: "flex-end" }}>
          {tech.evaluationModes.includes("chat") && <span className="badge b-blue" style={{ fontSize: 11 }}>💬 Chat</span>}
          {tech.evaluationModes.includes("presencial") && <span className="badge b-navy" style={{ fontSize: 11 }}>📅 Cita</span>}
        </div>
      </div>

      <div style={{ display: "flex", gap: 10 }}>
        <button className="btn btn-amber full" style={{ flex: 1, padding: "12px 16px", fontSize: 14 }} onClick={() => nav("eval", tech.id)}>
          Solicitar evaluación
        </button>
        <button className="btn btn-outline" style={{ flexShrink: 0, padding: "12px 14px" }} onClick={() => nav("profile", tech.id)}>
          Perfil
        </button>
      </div>
    </div>
  );
}

// ─── HOME PAGE ────────────────────────────────────────────────────────────────
function HomePage({ nav }) {
  return (
    <div>
      <section style={{ background: "linear-gradient(135deg,var(--navy) 0%,#1e3a5f 100%)", padding: "84px 16px 68px", position: "relative", overflow: "hidden" }}>
        <div style={{ position: "absolute", inset: 0, backgroundImage: "radial-gradient(circle at 70% 50%,rgba(212,134,11,.08) 0%,transparent 60%)", pointerEvents: "none" }} />
        <div className="con" style={{ position: "relative" }}>
          <div style={{ maxWidth: 640 }}>
            <div className="badge b-amber" style={{ marginBottom: 18, fontSize: 12 }}>🌡️ Hermosillo, Sonora</div>
            <h1 style={{ fontFamily: "var(--fd)", fontSize: "clamp(30px,5vw,52px)", fontWeight: 700, color: "white", lineHeight: 1.15, letterSpacing: "-1px", marginBottom: 16 }}>
              Encuentra técnicos de aire acondicionado <span style={{ color: "var(--amber-light)" }}>confiables</span> en Hermosillo
            </h1>
            <p style={{ fontSize: "clamp(14px,2vw,16px)", color: "rgba(255,255,255,.75)", marginBottom: 28, lineHeight: 1.7, maxWidth: 460 }}>
              Solicita una evaluación, compara presupuestos y paga de forma segura. TUCADI protege tu dinero hasta que el trabajo quede listo.
            </p>
            <div style={{ display: "flex", flexDirection: "column", gap: 12, maxWidth: 320 }}>
              <button className="btn btn-amber full" style={{ fontSize: 15, padding: "15px" }} onClick={() => nav("list")}>Ver técnicos disponibles →</button>
              <button className="btn btn-outline full" style={{ background: "transparent", color: "white", borderColor: "rgba(255,255,255,.3)" }} onClick={() => nav("how")}>¿Cómo funciona TUCADI?</button>
            </div>
          </div>
        </div>
      </section>

      <section className="sec-sm" style={{ background: "var(--bg-warm)", borderBottom: "1px solid var(--border)" }}>
        <div className="con">
          <div style={{ display: "grid", gridTemplateColumns: "repeat(auto-fit,minmax(200px,1fr))", gap: 24 }}>
            {[
              { i: "📍", t: "Técnicos locales", d: "Todos en Hermosillo. Sin intermediarios." },
              { i: "🔒", t: "Pago protegido 7 días", d: "Tu dinero se libera solo cuando el trabajo esté listo." },
              { i: "⭐", t: "Reseñas reales", d: "Solo clientes que pagaron pueden calificar." },
            ].map(b => (
              <div key={b.t} style={{ display: "flex", gap: 14, alignItems: "flex-start" }}>
                <div style={{ fontSize: 26, flexShrink: 0 }}>{b.i}</div>
                <div>
                  <div style={{ fontFamily: "var(--fd)", fontSize: 15, fontWeight: 600, color: "var(--navy)", marginBottom: 3 }}>{b.t}</div>
                  <div style={{ fontSize: 13, color: "var(--mid)", lineHeight: 1.6 }}>{b.d}</div>
                </div>
              </div>
            ))}
          </div>
        </div>
      </section>

      <section className="sec">
        <div className="con">
          <div style={{ display: "flex", justifyContent: "space-between", alignItems: "flex-end", marginBottom: 24, flexWrap: "wrap", gap: 12 }}>
            <div>
              <p style={{ fontSize: 11, fontWeight: 700, color: "var(--amber)", letterSpacing: "1.5px", textTransform: "uppercase", marginBottom: 6 }}>Aire acondicionado · Hermosillo</p>
              <h2 style={{ fontFamily: "var(--fd)", fontSize: "clamp(22px,3.5vw,30px)", fontWeight: 700, color: "var(--navy)" }}>Técnicos destacados</h2>
            </div>
            <button className="btn btn-outline" onClick={() => nav("list")}>Ver todos →</button>
          </div>
          <div style={{ display: "grid", gridTemplateColumns: "repeat(auto-fill,minmax(280px,1fr))", gap: 16 }}>
            {TECHNICIANS.slice(0, 3).map(t => <TechCard key={t.id} tech={t} nav={nav} />)}
          </div>
        </div>
      </section>

      <section className="sec-sm" style={{ background: "var(--bg-warm)", borderBottom: "1px solid var(--border)" }}>
        <div className="con" style={{ display: "flex", alignItems: "center", justifyContent: "space-between", gap: 20, flexWrap: "wrap" }}>
          <div>
            <h2 style={{ fontFamily: "var(--fd)", fontSize: "clamp(18px,3vw,26px)", fontWeight: 600, color: "var(--navy)", marginBottom: 8 }}>Tu dinero, protegido siempre</h2>
            <p style={{ fontSize: 14, color: "var(--mid)", maxWidth: 460, lineHeight: 1.7 }}>Cuando contratas un trabajo, TUCADI retiene el pago 7 días. Si hay algún problema, tienes ese tiempo para reportarlo.</p>
          </div>
          <button className="btn btn-navy" style={{ flexShrink: 0 }} onClick={() => nav("how")}>Ver cómo funciona</button>
        </div>
      </section>

      <section className="sec-sm" style={{ background: "linear-gradient(135deg,var(--navy) 0%,#1e3a5f 100%)" }}>
        <div className="con" style={{ display: "flex", alignItems: "center", justifyContent: "space-between", gap: 20, flexWrap: "wrap" }}>
          <div>
            <h2 style={{ fontFamily: "var(--fd)", fontSize: "clamp(16px,3vw,24px)", fontWeight: 600, color: "white", marginBottom: 8 }}>Hoy: aire acondicionado.<br />Mañana: todos los servicios locales.</h2>
            <p style={{ fontSize: 13, color: "rgba(255,255,255,.65)", maxWidth: 400, lineHeight: 1.7 }}>TUCADI comienza en Hermosillo con técnicos de minisplit. Pronto más categorías. La plataforma local de confianza para tu hogar.</p>
          </div>
          <button className="btn btn-amber" style={{ flexShrink: 0 }} onClick={() => nav("signup")}>Únete como técnico</button>
        </div>
      </section>
    </div>
  );
}

// ─── HOW IT WORKS ─────────────────────────────────────────────────────────────
function HowPage({ nav }) {
  return (
    <div>
      <div style={{ background: "var(--bg-warm)", borderBottom: "1px solid var(--border)", padding: "32px 16px" }}>
        <div className="con" style={{ maxWidth: 700 }}>
          <h1 style={{ fontFamily: "var(--fd)", fontSize: "clamp(24px,4vw,36px)", fontWeight: 700, color: "var(--navy)", marginBottom: 8 }}>¿Cómo funciona TUCADI?</h1>
          <p style={{ fontSize: 14, color: "var(--mid)", lineHeight: 1.7 }}>Un proceso claro y justo para clientes y técnicos.</p>
        </div>
      </div>

      <div className="sec" style={{ paddingTop: 36 }}>
        <div className="con" style={{ maxWidth: 700 }}>

          <h2 style={{ fontFamily: "var(--fd)", fontSize: 20, fontWeight: 700, color: "var(--navy)", marginBottom: 20 }}>Para clientes</h2>

          {[
            { n: "01", t: "Busca y elige un técnico", b: "Explora perfiles, lee reseñas reales y compara precios. Todos los técnicos son verificados y con calificaciones reales." },
            { n: "02", t: "Solicita una evaluación", b: "Antes del trabajo, el técnico evalúa el problema — por chat en la app o en persona (cita). El precio lo define el técnico.",
              extra: (
                <div className="fbox" style={{ marginTop: 12 }}>
                  <div className="fr"><span>Precio del técnico</span><span>Lo que defina (puede ser $0)</span></div>
                  <div className="fr" style={{ color: "var(--amber)" }}><span>Tarifa TUCADI (siempre aplica)</span><span style={{ fontWeight: 700 }}>${PLATFORM_FEE_EVAL} MXN</span></div>
                  <div className="fr-total"><span>Total evaluación</span><span>Precio técnico + ${PLATFORM_FEE_EVAL}</span></div>
                  <div style={{ fontSize: 11, color: "var(--muted)", marginTop: 8 }}>⚠️ TUCADI no retiene el precio del técnico. El $49 es tarifa de plataforma independiente.</div>
                </div>
              )
            },
            { n: "03", t: "Acepta el presupuesto y paga", b: "Después de evaluar, el técnico te envía el precio del trabajo. Si aceptas, pagas por la app. Tu dinero queda protegido — no llega al técnico todavía.",
              extra: (
                <div className="fbox" style={{ marginTop: 12 }}>
                  <div style={{ fontSize: 12, color: "var(--muted)", marginBottom: 8 }}>Ejemplo: trabajo de $1,000 MXN</div>
                  <div className="fr"><span>Tú pagas</span><span style={{ fontWeight: 700 }}>$1,000 MXN</span></div>
                  <div className="fr"><span>TUCADI retiene</span><span>{RETENTION_DAYS} días calendario</span></div>
                  <div className="fr"><span>Comisión TUCADI</span><span>10% = $100 MXN</span></div>
                  <div className="fr-tech"><span>🟢 Técnico recibe</span><span>$900 MXN</span></div>
                </div>
              )
            },
            { n: "04", t: "El trabajo se realiza", b: `El técnico realiza el servicio. Si quedas conforme, no haces nada — a los ${RETENTION_DAYS} días TUCADI libera el pago. Si hay un problema, tienes ese plazo para reportarlo.` },
            { n: "05", t: "Califica al técnico", b: "Solo los clientes que pagaron pueden dejar reseñas. Eso garantiza que las calificaciones son reales y confiables." },
          ].map((s, i, arr) => (
            <div key={s.n} style={{ display: "flex", gap: 18, marginBottom: 24 }}>
              <div style={{ display: "flex", flexDirection: "column", alignItems: "center" }}>
                <div style={{ width: 34, height: 34, borderRadius: "50%", background: "var(--navy)", color: "white", display: "flex", alignItems: "center", justifyContent: "center", fontFamily: "var(--fd)", fontWeight: 700, fontSize: 13, flexShrink: 0 }}>{s.n}</div>
                {i < arr.length - 1 && <div style={{ width: 2, flex: 1, minHeight: 20, background: "var(--border)", marginTop: 6 }} />}
              </div>
              <div style={{ flex: 1, paddingBottom: 6 }}>
                <h3 style={{ fontFamily: "var(--fd)", fontSize: 17, fontWeight: 600, color: "var(--navy)", marginBottom: 5 }}>{s.t}</h3>
                <p style={{ fontSize: 14, color: "var(--mid)", lineHeight: 1.7 }}>{s.b}</p>
                {s.extra}
              </div>
            </div>
          ))}

          <div className="divider" style={{ margin: "32px 0" }} />

          <h2 style={{ fontFamily: "var(--fd)", fontSize: 20, fontWeight: 700, color: "var(--navy)", marginBottom: 16 }}>Para técnicos</h2>
          <div className="card-flat" style={{ padding: "20px 22px", marginBottom: 20 }}>
            <h3 style={{ fontFamily: "var(--fd)", fontSize: 16, fontWeight: 600, color: "var(--navy)", marginBottom: 12 }}>Tú controlas tus precios</h3>
            {[
              "Defines el precio de tu evaluación — puede ser $0 o lo que quieras. Además siempre se cobra al cliente $49 MXN de tarifa de plataforma TUCADI, que no te corresponde a ti.",
              "Después de evaluar, defines el precio del trabajo. El cliente acepta o no — sin presiones.",
              "Recibes el 90% de cada trabajo. TUCADI retiene el 10% como comisión de plataforma.",
              `El dinero se libera a los ${RETENTION_DAYS} días — tiempo para que el cliente confirme que todo quedó bien.`,
            ].map((t, i) => (
              <div key={i} style={{ display: "flex", gap: 10, fontSize: 14, color: "var(--mid)", marginBottom: 8 }}>
                <span style={{ color: "var(--green)", fontWeight: 700 }}>✓</span><span>{t}</span>
              </div>
            ))}
          </div>

          <div className="fbox" style={{ marginBottom: 28 }}>
            <p style={{ fontWeight: 700, color: "var(--navy)", marginBottom: 10, fontSize: 14 }}>Desglose para el técnico (trabajo de $1,500 MXN):</p>
            <div className="fr"><span>Trabajo acordado</span><span>$1,500 MXN</span></div>
            <div className="fr"><span>Comisión TUCADI (10%)</span><span>- $150 MXN</span></div>
            <div className="fr-tech"><span>🟢 Recibes en {RETENTION_DAYS} días</span><span>$1,350 MXN</span></div>
          </div>

          <div style={{ display: "flex", gap: 12, flexWrap: "wrap" }}>
            <button className="btn btn-navy" onClick={() => nav("list")}>Buscar técnico</button>
            <button className="btn btn-outline" onClick={() => nav("signup")}>Unirme como técnico</button>
          </div>
        </div>
      </div>
    </div>
  );
}

// ─── LIST PAGE ────────────────────────────────────────────────────────────────
function ListPage({ nav }) {
  const [search, setSearch] = useState("");
  const [svc, setSvc] = useState("");
  const [zone, setZone] = useState("");
  const [rating, setRating] = useState("");
  const [open, setOpen] = useState(false);
  const zones = [...new Set(TECHNICIANS.map(t => t.zone))];
  const active = [svc, zone, rating].filter(Boolean).length;
  const list = TECHNICIANS.filter(t => {
    if (search && !t.name.toLowerCase().includes(search.toLowerCase()) && !t.description.toLowerCase().includes(search.toLowerCase())) return false;
    if (svc && !t.services.includes(svc)) return false;
    if (zone && t.zone !== zone) return false;
    if (rating && t.rating < parseFloat(rating)) return false;
    return true;
  });

  return (
    <div>
      <div style={{ background: "var(--bg-warm)", borderBottom: "1px solid var(--border)", padding: "26px 16px" }}>
        <div className="con">
          <div style={{ display: "flex", gap: 8, alignItems: "center", marginBottom: 6 }}>
            <span className="badge b-navy">Aire acondicionado</span>
            <span style={{ fontSize: 13, color: "var(--muted)" }}>· Hermosillo</span>
          </div>
          <h1 style={{ fontFamily: "var(--fd)", fontSize: "clamp(22px,4vw,30px)", fontWeight: 700, color: "var(--navy)", marginBottom: 4 }}>Técnicos disponibles</h1>
          <p style={{ fontSize: 13, color: "var(--mid)" }}>{TECHNICIANS.length} técnicos verificados</p>
        </div>
      </div>

      <div style={{ background: "white", borderBottom: "1px solid var(--border)", position: "sticky", top: 56, zIndex: 90 }}>
        <div className="con" style={{ padding: "12px 16px" }}>
          <div style={{ display: "flex", gap: 10, alignItems: "center" }}>
            <input className="inp" placeholder="🔍  Buscar técnico..." value={search} onChange={e => setSearch(e.target.value)} style={{ flex: 1 }} />
            <button className="btn btn-outline" style={{ flexShrink: 0, padding: "11px 14px", position: "relative", gap: 6 }} onClick={() => setOpen(o => !o)}>
              <svg width="15" height="15" viewBox="0 0 24 24" fill="none" stroke="currentColor" strokeWidth="2"><line x1="4" y1="6" x2="20" y2="6"/><line x1="8" y1="12" x2="16" y2="12"/><line x1="10" y1="18" x2="14" y2="18"/></svg>
              Filtros
              {active > 0 && <span style={{ position: "absolute", top: -6, right: -6, background: "var(--amber)", color: "white", borderRadius: "50%", width: 18, height: 18, fontSize: 11, fontWeight: 700, display: "flex", alignItems: "center", justifyContent: "center" }}>{active}</span>}
            </button>
          </div>
          {open && (
            <div style={{ display: "grid", gridTemplateColumns: "repeat(auto-fill,minmax(150px,1fr))", gap: 10, marginTop: 12, paddingTop: 12, borderTop: "1px solid var(--border)" }}>
              <select className="sel" value={svc} onChange={e => setSvc(e.target.value)}>
                <option value="">Todos los servicios</option>
                <option>Instalación</option><option>Reparación</option><option>Mantenimiento</option>
              </select>
              <select className="sel" value={zone} onChange={e => setZone(e.target.value)}>
                <option value="">Todas las zonas</option>
                {zones.map(z => <option key={z}>{z}</option>)}
              </select>
              <select className="sel" value={rating} onChange={e => setRating(e.target.value)}>
                <option value="">Cualquier calificación</option>
                <option value="4.8">4.8+ ⭐</option><option value="4.5">4.5+ ⭐</option><option value="4.0">4.0+ ⭐</option>
              </select>
              {active > 0 && <button className="btn btn-outline" style={{ fontSize: 13, padding: "10px 14px" }} onClick={() => { setSvc(""); setZone(""); setRating(""); }}>✕ Limpiar</button>}
            </div>
          )}
        </div>
      </div>

      <div style={{ padding: "20px 16px 56px" }}>
        <div className="con">
          {list.length === 0 ? (
            <div style={{ textAlign: "center", padding: "60px 0", color: "var(--muted)" }}>
              <div style={{ fontSize: 40, marginBottom: 12 }}>🔍</div>
              <p>No se encontraron técnicos con esos filtros.</p>
              <button className="btn btn-outline" style={{ marginTop: 16 }} onClick={() => { setSearch(""); setSvc(""); setZone(""); setRating(""); }}>Limpiar filtros</button>
            </div>
          ) : (
            <>
              <p style={{ fontSize: 13, color: "var(--muted)", marginBottom: 16 }}>{list.length} técnico{list.length !== 1 ? "s" : ""} encontrado{list.length !== 1 ? "s" : ""}</p>
              <div style={{ display: "grid", gridTemplateColumns: "repeat(auto-fill,minmax(280px,1fr))", gap: 16 }}>
                {list.map(t => <TechCard key={t.id} tech={t} nav={nav} />)}
              </div>
            </>
          )}
        </div>
      </div>
    </div>
  );
}

// ─── EVAL FLOW ────────────────────────────────────────────────────────────────
function EvalPage({ techId, nav }) {
  const tech = TECHNICIANS.find(t => t.id === techId);
  const [step, setStep] = useState(1);
  const [mode, setMode] = useState(null);
  const [chatMsg, setChatMsg] = useState("");
  const [chatLog, setChatLog] = useState([
    { from: "tech", text: `Hola, soy ${tech?.name.split(" ")[0]}. ¿En qué te puedo ayudar? Cuéntame el problema con tu equipo.` }
  ]);
  const [date, setDate] = useState("");
  const [time, setTime] = useState("");
  const [address, setAddress] = useState("");
  const [booked, setBooked] = useState(false);
  const [selectedJob, setSelectedJob] = useState(null);

  if (!tech) return null;
  const free = tech.evaluationPrice === 0;
  const evalTotal = tech.evaluationPrice + PLATFORM_FEE_EVAL;

  const sendChat = () => {
    if (!chatMsg.trim()) return;
    const msg = chatMsg;
    setChatMsg("");
    setChatLog(l => [...l, { from: "me", text: msg }]);
    setTimeout(() => {
      setChatLog(l => [...l, { from: "tech", text: "Entendido. Con base en lo que describes, puedo darte un diagnóstico aquí mismo o ir a revisarlo en persona. Una vez evaluado te envío el presupuesto formal." }]);
    }, 900);
  };

  return (
    <div>
      <div style={{ padding: "13px 16px", background: "white", borderBottom: "1px solid var(--border)" }}>
        <div className="con"><button className="btn btn-ghost" style={{ padding: 0, gap: 5, color: "var(--mid)", fontSize: 14 }} onClick={() => nav("profile", techId)}>← Volver al perfil</button></div>
      </div>

      <div style={{ padding: "24px 16px 56px" }}>
        <div className="con" style={{ maxWidth: 540 }}>

          {/* Step track */}
          <div className="strack">
            {["Modo", "Evaluar", "Confirmar"].map((lbl, i) => {
              const idx = i + 1;
              const cls = step === 1 ? (idx === 1 ? "sd-active" : "sd-pending") : step === 2 || step === 3 ? (idx < 2 ? "sd-done" : idx === 2 ? "sd-active" : "sd-pending") : idx < 3 ? "sd-done" : "sd-active";
              return (
                <div key={lbl} style={{ display: "flex", alignItems: "center", flex: i < 2 ? 1 : "none" }}>
                  <div style={{ display: "flex", flexDirection: "column", alignItems: "center", gap: 4 }}>
                    <div className={`sdot ${cls}`}>{cls === "sd-done" ? "✓" : idx}</div>
                    <div style={{ fontSize: 11, color: cls === "sd-active" ? "var(--amber)" : "var(--muted)", fontWeight: 600, whiteSpace: "nowrap" }}>{lbl}</div>
                  </div>
                  {i < 2 && <div className={`sline${cls === "sd-done" ? " sl-done" : ""}`} style={{ marginBottom: 20 }} />}
                </div>
              );
            })}
          </div>

          {/* Tech mini */}
          <div style={{ display: "flex", gap: 14, alignItems: "center", marginBottom: 24, background: "var(--bg-warm)", borderRadius: "var(--rs)", padding: "14px 16px", border: "1px solid var(--border)" }}>
            <div className="av" style={{ background: tech.avatarColor }}>{tech.avatar}</div>
            <div>
              <div style={{ fontFamily: "var(--fd)", fontWeight: 600, color: "var(--navy)", fontSize: 15 }}>{tech.name}</div>
              <div style={{ fontSize: 13, color: "var(--muted)" }}>⭐ {tech.rating} · {tech.zone}</div>
            </div>
          </div>

          {/* STEP 1 */}
          {step === 1 && (
            <div>
              <h2 style={{ fontFamily: "var(--fd)", fontSize: 20, fontWeight: 700, color: "var(--navy)", marginBottom: 6 }}>¿Cómo quieres que te evalúe?</h2>
              <p style={{ fontSize: 14, color: "var(--mid)", marginBottom: 20, lineHeight: 1.6 }}>El técnico revisará el problema y te dará un diagnóstico antes de cualquier trabajo.</p>

              <div className="fbox" style={{ marginBottom: 20 }}>
                <div className="fr"><span>Precio del técnico</span><span style={{ fontWeight: 700, color: free ? "var(--green)" : "var(--navy)" }}>{free ? "Gratis" : fmt(tech.evaluationPrice)}</span></div>
                <div className="fr" style={{ color: "var(--amber)" }}><span>Tarifa de plataforma TUCADI</span><span style={{ fontWeight: 700 }}>{fmt(PLATFORM_FEE_EVAL)}</span></div>
                <div className="fr-total"><span>Total evaluación</span><span>{fmt(evalTotal)}</span></div>
                <p style={{ fontSize: 11, color: "var(--muted)", marginTop: 8, lineHeight: 1.5 }}>La tarifa de plataforma TUCADI siempre aplica. El precio del técnico le corresponde íntegro a él — TUCADI no lo retiene.</p>
              </div>

              <div style={{ display: "flex", flexDirection: "column", gap: 12 }}>
                {tech.evaluationModes.includes("chat") && (
                  <button style={{ padding: "18px 20px", textAlign: "left", cursor: "pointer", border: `${mode === "chat" ? "2px solid var(--navy)" : "1px solid var(--border)"}`, borderRadius: "var(--r)", background: mode === "chat" ? "rgba(15,37,64,.03)" : "white", width: "100%" }}
                    onClick={() => setMode("chat")}>
                    <div style={{ display: "flex", justifyContent: "space-between", alignItems: "center" }}>
                      <div>
                        <div style={{ fontWeight: 700, fontSize: 15, color: "var(--navy)", marginBottom: 4 }}>💬 Evaluación por chat</div>
                        <div style={{ fontSize: 13, color: "var(--mid)" }}>Escríbele directamente. Define el problema y el técnico te cotiza.</div>
                      </div>
                      {mode === "chat" && <span style={{ fontSize: 20, color: "var(--navy)" }}>✓</span>}
                    </div>
                  </button>
                )}
                {tech.evaluationModes.includes("presencial") && (
                  <button style={{ padding: "18px 20px", textAlign: "left", cursor: "pointer", border: `${mode === "presencial" ? "2px solid var(--navy)" : "1px solid var(--border)"}`, borderRadius: "var(--r)", background: mode === "presencial" ? "rgba(15,37,64,.03)" : "white", width: "100%" }}
                    onClick={() => setMode("presencial")}>
                    <div style={{ display: "flex", justifyContent: "space-between", alignItems: "center" }}>
                      <div>
                        <div style={{ fontWeight: 700, fontSize: 15, color: "var(--navy)", marginBottom: 4 }}>📅 Visita presencial</div>
                        <div style={{ fontSize: 13, color: "var(--mid)" }}>El técnico va a tu domicilio a revisar el equipo en persona.</div>
                      </div>
                      {mode === "presencial" && <span style={{ fontSize: 20, color: "var(--navy)" }}>✓</span>}
                    </div>
                  </button>
                )}
              </div>

              <button style={{ marginTop: 24, width: "100%", padding: "14px", fontSize: 15, background: !mode ? "var(--border)" : "var(--navy)", color: !mode ? "var(--muted)" : "white", borderRadius: "var(--rs)", border: "none", fontFamily: "var(--fb)", fontWeight: 700, cursor: mode ? "pointer" : "default" }}
                onClick={() => mode && setStep(mode === "chat" ? 2 : 3)}>
                Continuar →
              </button>
            </div>
          )}

          {/* STEP 2 — chat */}
          {step === 2 && (
            <div>
              <h2 style={{ fontFamily: "var(--fd)", fontSize: 20, fontWeight: 700, color: "var(--navy)", marginBottom: 4 }}>Chat con {tech.name.split(" ")[0]}</h2>
              <p style={{ fontSize: 13, color: "var(--muted)", marginBottom: 16 }}>Describe el problema y acuerda el diagnóstico aquí.</p>
              <div style={{ background: "var(--bg-warm)", borderRadius: "var(--r)", border: "1px solid var(--border)", padding: 16, marginBottom: 14, minHeight: 200, display: "flex", flexDirection: "column", gap: 12 }}>
                {chatLog.map((m, i) => (
                  <div key={i} className={`bubble ${m.from === "me" ? "b-me" : "b-them"}`}>{m.text}</div>
                ))}
              </div>
              <div style={{ display: "flex", gap: 10, marginBottom: 14 }}>
                <input className="inp" value={chatMsg} onChange={e => setChatMsg(e.target.value)} placeholder="Escribe un mensaje..." onKeyDown={e => e.key === "Enter" && sendChat()} />
                <button className="btn btn-navy" style={{ flexShrink: 0, padding: "12px 16px" }} onClick={sendChat}>Enviar</button>
              </div>
              <div className="alert al-info" style={{ marginBottom: 14 }}>💡 Cuando estén de acuerdo, el técnico te enviará el presupuesto formal desde su perfil.</div>
              <button className="btn btn-amber full" style={{ padding: "13px" }} onClick={() => setStep(4)}>Terminar evaluación y ver presupuesto →</button>
            </div>
          )}

          {/* STEP 3 — schedule */}
          {step === 3 && !booked && (
            <div>
              <h2 style={{ fontFamily: "var(--fd)", fontSize: 20, fontWeight: 700, color: "var(--navy)", marginBottom: 4 }}>Agendar visita presencial</h2>
              <p style={{ fontSize: 13, color: "var(--muted)", marginBottom: 20 }}>Elige el día y hora. Se creará una actividad pendiente para ambos.</p>
              <div style={{ display: "flex", flexDirection: "column", gap: 16 }}>
                <div><label className="lbl">Fecha *</label><input className="inp" type="date" value={date} onChange={e => setDate(e.target.value)} min={new Date().toISOString().split("T")[0]} /></div>
                <div><label className="lbl">Hora *</label>
                  <select className="sel" value={time} onChange={e => setTime(e.target.value)}>
                    <option value="">Selecciona una hora...</option>
                    {["08:00","09:00","10:00","11:00","12:00","13:00","14:00","15:00","16:00","17:00","18:00"].map(h => <option key={h} value={h}>{h} hrs</option>)}
                  </select>
                </div>
                <div><label className="lbl">Dirección *</label><input className="inp" placeholder="Ej. Calle Sinaloa 204, Col. Centro" value={address} onChange={e => setAddress(e.target.value)} /></div>
                <div className="fbox">
                  <div className="fr"><span>Precio del técnico</span><span style={{ fontWeight: 700, color: free ? "var(--green)" : "var(--navy)" }}>{free ? "Gratis" : fmt(tech.evaluationPrice)}</span></div>
                  <div className="fr" style={{ color: "var(--amber)" }}><span>Tarifa TUCADI</span><span>{fmt(PLATFORM_FEE_EVAL)}</span></div>
                  <div className="fr-total"><span>Total a pagar</span><span>{fmt(evalTotal)}</span></div>
                </div>
                <button className="btn btn-amber full" style={{ padding: "14px", fontSize: 15 }} onClick={() => { if (date && time && address) setBooked(true); }}>
                  Confirmar cita y pagar {fmt(evalTotal)}
                </button>
              </div>
            </div>
          )}

          {/* Booked */}
          {step === 3 && booked && (
            <div style={{ textAlign: "center", paddingTop: 8 }}>
              <div style={{ fontSize: 52, marginBottom: 14 }}>📅</div>
              <h2 style={{ fontFamily: "var(--fd)", fontSize: 22, fontWeight: 700, color: "var(--navy)", marginBottom: 10 }}>¡Cita confirmada!</h2>
              <p style={{ fontSize: 14, color: "var(--mid)", lineHeight: 1.7, marginBottom: 22 }}>
                {tech.name.split(" ")[0]} llegará el <strong>{date}</strong> a las <strong>{time} hrs</strong>.<br />
                Se creó una actividad pendiente en tu cuenta y en la del técnico.
              </p>
              <div className="acard" style={{ textAlign: "left", marginBottom: 20 }}>
                <div style={{ display: "flex", justifyContent: "space-between", alignItems: "flex-start", marginBottom: 14 }}>
                  <div>
                    <div style={{ fontSize: 11, fontWeight: 700, color: "var(--amber)", letterSpacing: "1px", textTransform: "uppercase" }}>Actividad pendiente</div>
                    <div style={{ fontFamily: "var(--fd)", fontSize: 17, fontWeight: 600, color: "var(--navy)", marginTop: 4 }}>Evaluación presencial</div>
                  </div>
                  <span className="badge b-amber">Pendiente</span>
                </div>
                {[["🧑‍🔧", tech.name], ["📅", `${date} · ${time} hrs`], ["📍", address], ["💳", `Evaluación: ${fmt(evalTotal)} (pagado)`]].map(([icon, val]) => (
                  <div key={val} style={{ fontSize: 13, color: "var(--mid)", marginBottom: 6, display: "flex", gap: 8 }}>
                    <span>{icon}</span><span>{val}</span>
                  </div>
                ))}
              </div>
              <div className="alert al-info" style={{ textAlign: "left", marginBottom: 18 }}>💡 Después de la visita, el técnico te enviará el presupuesto. Podrás aceptarlo y pagar desde la app.</div>
              <button className="btn btn-navy full" style={{ padding: "14px" }} onClick={() => nav("profile", techId)}>Ver perfil del técnico</button>
            </div>
          )}

          {/* STEP 4 — post-chat budget */}
          {step === 4 && (
            <div>
              <h2 style={{ fontFamily: "var(--fd)", fontSize: 20, fontWeight: 700, color: "var(--navy)", marginBottom: 4 }}>Presupuesto del técnico</h2>
              <p style={{ fontSize: 13, color: "var(--muted)", marginBottom: 18 }}>Basado en la evaluación por chat, {tech.name.split(" ")[0]} propone:</p>
              <div style={{ display: "flex", flexDirection: "column", gap: 12, marginBottom: 18 }}>
                {tech.jobs.map(j => {
                  const sel = selectedJob === j.id;
                  return (
                    <div key={j.id} style={{ border: `${sel ? "2px solid var(--navy)" : "1px solid var(--border)"}`, borderRadius: "var(--rs)", padding: "14px 16px", cursor: "pointer", background: sel ? "rgba(15,37,64,.02)" : "white" }}
                      onClick={() => setSelectedJob(sel ? null : j.id)}>
                      <div style={{ display: "flex", justifyContent: "space-between", alignItems: "flex-start", gap: 10 }}>
                        <div style={{ flex: 1 }}>
                          <div style={{ fontWeight: 700, fontSize: 15, color: "var(--navy)" }}>{j.name}</div>
                          <div style={{ fontSize: 13, color: "var(--mid)", marginTop: 3 }}>{j.desc}</div>
                        </div>
                        <div style={{ textAlign: "right", flexShrink: 0 }}>
                          <div style={{ fontFamily: "var(--fd)", fontWeight: 800, fontSize: 17, color: "var(--navy)" }}>{fmt(j.price)}</div>
                          <div style={{ fontSize: 11, color: "var(--muted)" }}>técnico recibe {fmt(Math.round(j.price * (1 - TUCADI_FEE_PCT)))}</div>
                        </div>
                      </div>
                      {sel && (
                        <div style={{ marginTop: 12 }}>
                          <div className="fbox" style={{ marginBottom: 12 }}>
                            <div className="fr"><span>Precio del trabajo</span><span style={{ fontWeight: 700 }}>{fmt(j.price)}</span></div>
                            <div className="fr"><span>Comisión TUCADI (10%)</span><span>- {fmt(Math.round(j.price * TUCADI_FEE_PCT))}</span></div>
                            <div className="fr"><span>Retención</span><span>{RETENTION_DAYS} días</span></div>
                            <div className="fr-tech"><span>🟢 Técnico recibe</span><span>{fmt(Math.round(j.price * (1 - TUCADI_FEE_PCT)))}</span></div>
                          </div>
                          <button className="btn btn-amber full" style={{ fontSize: 14, padding: "12px" }} onClick={() => nav("profile", techId)}>Aceptar y pagar {fmt(j.price)} →</button>
                        </div>
                      )}
                    </div>
                  );
                })}
              </div>
              <button className="btn btn-ghost full" onClick={() => nav("profile", techId)}>Ver todos los servicios del técnico</button>
            </div>
          )}
        </div>
      </div>
    </div>
  );
}

// ─── PROFILE PAGE ─────────────────────────────────────────────────────────────
function ProfilePage({ techId, nav }) {
  const tech = TECHNICIANS.find(t => t.id === techId);
  const reviews = REVIEWS[techId] || [];
  const [selJob, setSelJob] = useState(null);
  if (!tech) return null;
  const free = tech.evaluationPrice === 0;

  return (
    <div className="has-wafloat">
      <div style={{ padding: "13px 16px", background: "white", borderBottom: "1px solid var(--border)" }}>
        <div className="con"><button className="btn btn-ghost" style={{ padding: 0, fontSize: 14, color: "var(--mid)", gap: 5 }} onClick={() => nav("list")}>← Volver a técnicos</button></div>
      </div>

      <div style={{ background: "var(--bg-warm)", borderBottom: "1px solid var(--border)", padding: "26px 16px" }}>
        <div className="con">
          <div style={{ display: "flex", gap: 18, alignItems: "flex-start", flexWrap: "wrap" }}>
            <div className="av av-lg" style={{ background: tech.avatarColor }}>{tech.avatar}</div>
            <div style={{ flex: 1, minWidth: 200 }}>
              <h1 style={{ fontFamily: "var(--fd)", fontSize: "clamp(20px,4vw,28px)", fontWeight: 700, color: "var(--navy)", marginBottom: 6 }}>{tech.name}</h1>
              <div style={{ display: "flex", alignItems: "center", gap: 8, flexWrap: "wrap", marginBottom: 6 }}>
                <span style={{ color: "var(--amber-light)", fontSize: 14 }}>{"★".repeat(Math.floor(tech.rating))}</span>
                <span style={{ fontWeight: 700, fontSize: 14, color: "var(--navy)" }}>{tech.rating}</span>
                <span style={{ fontSize: 13, color: "var(--muted)" }}>({tech.reviewCount} reseñas)</span>
                <span className="badge b-amber">{tech.experienceYears} años exp.</span>
              </div>
              <div style={{ fontSize: 13, color: "var(--mid)" }}>📍 {tech.zone}</div>
            </div>
            <button className="btn btn-amber hide-mobile" onClick={() => nav("eval", tech.id)}>Solicitar evaluación</button>
          </div>
        </div>
      </div>

      <div style={{ padding: "20px 16px 56px" }}>
        <div className="con">
          <div style={{ display: "grid", gridTemplateColumns: "1fr 290px", gap: 24, alignItems: "start" }}>
            <div>
              {/* Eval info */}
              <div className="card-flat" style={{ padding: "18px 20px", marginBottom: 16 }}>
                <h2 style={{ fontFamily: "var(--fd)", fontSize: 17, fontWeight: 600, color: "var(--navy)", marginBottom: 12 }}>Evaluación</h2>
                <div style={{ display: "flex", justifyContent: "space-between", alignItems: "center", flexWrap: "wrap", gap: 10 }}>
                  <div>
                    <div style={{ fontSize: 22, fontWeight: 800, fontFamily: "var(--fd)", color: free ? "var(--green)" : "var(--navy)" }}>{free ? "Gratis" : fmt(tech.evaluationPrice)}</div>
                    <div style={{ fontSize: 12, color: "var(--amber)", fontWeight: 600, marginTop: 3 }}>+ {fmt(PLATFORM_FEE_EVAL)} tarifa de plataforma TUCADI</div>
                  </div>
                  <div style={{ display: "flex", gap: 6, flexWrap: "wrap" }}>
                    {tech.evaluationModes.includes("chat") && <span className="badge b-blue">💬 Chat</span>}
                    {tech.evaluationModes.includes("presencial") && <span className="badge b-navy">📅 En persona</span>}
                  </div>
                </div>
                <p style={{ fontSize: 12, color: "var(--muted)", marginTop: 10 }}>La tarifa de plataforma TUCADI ({fmt(PLATFORM_FEE_EVAL)}) siempre aplica. El precio del técnico le corresponde íntegro a él.</p>
              </div>

              {/* Jobs */}
              <div className="card-flat" style={{ padding: "18px 20px", marginBottom: 16 }}>
                <h2 style={{ fontFamily: "var(--fd)", fontSize: 17, fontWeight: 600, color: "var(--navy)", marginBottom: 4 }}>Trabajos y precios</h2>
                <p style={{ fontSize: 12, color: "var(--muted)", marginBottom: 16 }}>Precios definidos por el técnico. TUCADI retiene {RETENTION_DAYS} días y cobra 10% de comisión.</p>
                <div style={{ display: "flex", flexDirection: "column", gap: 12 }}>
                  {tech.jobs.map(j => {
                    const techGets = Math.round(j.price * (1 - TUCADI_FEE_PCT));
                    const sel = selJob === j.id;
                    return (
                      <div key={j.id} style={{ border: `${sel ? "2px solid var(--navy)" : "1.5px solid var(--border)"}`, borderRadius: "var(--rs)", padding: "14px 16px", cursor: "pointer", background: sel ? "rgba(15,37,64,.02)" : "white" }}
                        onClick={() => setSelJob(sel ? null : j.id)}>
                        <div style={{ display: "flex", justifyContent: "space-between", alignItems: "flex-start", gap: 10 }}>
                          <div style={{ flex: 1 }}>
                            <div style={{ fontWeight: 700, fontSize: 15, color: "var(--navy)" }}>{j.name}</div>
                            <div style={{ fontSize: 13, color: "var(--mid)", marginTop: 3, lineHeight: 1.5 }}>{j.desc}</div>
                          </div>
                          <div style={{ textAlign: "right", flexShrink: 0 }}>
                            <div style={{ fontFamily: "var(--fd)", fontWeight: 800, fontSize: 17, color: "var(--navy)" }}>{fmt(j.price)}</div>
                            <div style={{ fontSize: 11, color: "var(--muted)" }}>técnico recibe {fmt(techGets)}</div>
                          </div>
                        </div>
                        {sel && (
                          <div style={{ marginTop: 12 }}>
                            <div className="fbox" style={{ marginBottom: 12 }}>
                              <div className="fr"><span>Precio del trabajo</span><span style={{ fontWeight: 700 }}>{fmt(j.price)}</span></div>
                              <div className="fr"><span>Comisión TUCADI (10%)</span><span>- {fmt(Math.round(j.price * TUCADI_FEE_PCT))}</span></div>
                              <div className="fr"><span>Retención</span><span>{RETENTION_DAYS} días</span></div>
                              <div className="fr-tech"><span>🟢 Técnico recibe</span><span>{fmt(techGets)}</span></div>
                            </div>
                            <button className="btn btn-amber full" style={{ fontSize: 14, padding: "12px" }} onClick={e => { e.stopPropagation(); nav("eval", tech.id); }}>Contratar este servicio →</button>
                          </div>
                        )}
                      </div>
                    );
                  })}
                </div>
              </div>

              {/* About */}
              <div className="card-flat" style={{ padding: "18px 20px", marginBottom: 16 }}>
                <h2 style={{ fontFamily: "var(--fd)", fontSize: 17, fontWeight: 600, color: "var(--navy)", marginBottom: 10 }}>Sobre {tech.name.split(" ")[0]}</h2>
                <p style={{ fontSize: 14, color: "var(--mid)", lineHeight: 1.8 }}>{tech.description}</p>
              </div>

              {/* Stats */}
              <div className="card-flat" style={{ padding: "16px 20px", marginBottom: 16 }}>
                <div style={{ display: "grid", gridTemplateColumns: "repeat(3,1fr)", gap: 12, textAlign: "center" }}>
                  {[["⭐ " + tech.rating, "Calificación"], [tech.reviewCount, "Reseñas"], [tech.experienceYears + " años", "Experiencia"]].map(([v, l]) => (
                    <div key={l}><div style={{ fontFamily: "var(--fd)", fontSize: 17, fontWeight: 700, color: "var(--navy)" }}>{v}</div><div style={{ fontSize: 11, color: "var(--muted)", marginTop: 2 }}>{l}</div></div>
                  ))}
                </div>
              </div>

              {/* Reviews */}
              <h2 style={{ fontFamily: "var(--fd)", fontSize: 17, fontWeight: 600, color: "var(--navy)", marginBottom: 14 }}>Reseñas ({reviews.length})</h2>
              <div style={{ display: "flex", flexDirection: "column", gap: 12 }}>
                {reviews.map((r, i) => (
                  <div key={i} className="card-flat" style={{ padding: "15px 18px" }}>
                    <div style={{ display: "flex", justifyContent: "space-between", marginBottom: 6, flexWrap: "wrap", gap: 6 }}>
                      <span style={{ fontWeight: 600, fontSize: 14, color: "var(--navy)" }}>{r.userName}</span>
                      <span style={{ color: "var(--amber-light)", fontSize: 13 }}>{"★".repeat(r.rating)}</span>
                    </div>
                    <p style={{ fontSize: 13, color: "var(--mid)", lineHeight: 1.7 }}>{r.comment}</p>
                  </div>
                ))}
              </div>
            </div>

            {/* Sidebar — hidden on mobile via CSS */}
            <div className="hide-mobile" style={{ position: "sticky", top: 76 }}>
              <div className="card" style={{ padding: 22 }}>
                <h3 style={{ fontFamily: "var(--fd)", fontSize: 17, fontWeight: 600, color: "var(--navy)", marginBottom: 6 }}>¿Listo para empezar?</h3>
                <p style={{ fontSize: 13, color: "var(--muted)", marginBottom: 18, lineHeight: 1.6 }}>Primero agenda una evaluación. Sin compromiso.</p>
                <button className="btn btn-amber full" style={{ marginBottom: 10 }} onClick={() => nav("eval", tech.id)}>Solicitar evaluación</button>
                <a href={`https://wa.me/52${tech.phone}`} target="_blank" rel="noopener noreferrer" className="btn btn-wa-lg"><WA /> WhatsApp directo</a>
                <div className="divider" />
                <div style={{ display: "flex", flexDirection: "column", gap: 10 }}>
                  {[["Evaluación (técnico)", free ? "Gratis" : fmt(tech.evaluationPrice)], ["Tarifa TUCADI", fmt(PLATFORM_FEE_EVAL)], ["Total evaluación", fmt(tech.evaluationPrice + PLATFORM_FEE_EVAL)], ["Comisión TUCADI","10% del trabajo"], ["Retención del pago",`${RETENTION_DAYS} días`], ["Zona", tech.zone]].map(([l, v]) => (
                    <div key={l} style={{ display: "flex", justifyContent: "space-between", fontSize: 13 }}>
                      <span style={{ color: "var(--muted)" }}>{l}</span>
                      <span style={{ fontWeight: 600, color: "var(--navy)", textAlign: "right", maxWidth: 150 }}>{v}</span>
                    </div>
                  ))}
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>

      {/* Mobile float bar */}
      <div className="wafloat">
        <div style={{ flex: 1 }}>
          <div style={{ fontWeight: 600, fontSize: 14, color: "var(--navy)" }}>{tech.name}</div>
          <div style={{ fontSize: 12, color: "var(--muted)" }}>Eval: {free ? "Gratis" : fmt(tech.evaluationPrice)} + {fmt(PLATFORM_FEE_EVAL)} TUCADI = {fmt(tech.evaluationPrice + PLATFORM_FEE_EVAL)}</div>
        </div>
        <button className="btn btn-amber" style={{ flexShrink: 0, padding: "12px 18px", fontSize: 14 }} onClick={() => nav("eval", tech.id)}>Solicitar →</button>
      </div>
    </div>
  );
}

// ─── SIGNUP PAGE ──────────────────────────────────────────────────────────────
function SignupPage() {
  const [f, setF] = useState({ name: "", business: "", phone: "", services: [], experience: "", zone: "", evalPrice: "", description: "" });
  const [done, setDone] = useState(false);
  const svcs = ["Instalación", "Reparación", "Mantenimiento"];
  const tog = (s) => setF(p => ({ ...p, services: p.services.includes(s) ? p.services.filter(x => x !== s) : [...p.services, s] }));

  if (done) return (
    <div style={{ minHeight: "60vh", display: "flex", alignItems: "center", justifyContent: "center", padding: 24 }}>
      <div style={{ textAlign: "center", maxWidth: 380 }}>
        <div style={{ fontSize: 52, marginBottom: 14 }}>🎉</div>
        <h2 style={{ fontFamily: "var(--fd)", fontSize: 24, fontWeight: 700, color: "var(--navy)", marginBottom: 10 }}>¡Gracias por registrarte!</h2>
        <p style={{ fontSize: 14, color: "var(--mid)", lineHeight: 1.7 }}>Hemos recibido tu solicitud. Nos pondremos en contacto pronto para activar tu perfil.</p>
      </div>
    </div>
  );

  return (
    <div>
      <div style={{ background: "var(--bg-warm)", borderBottom: "1px solid var(--border)", padding: "28px 16px" }}>
        <div className="con" style={{ maxWidth: 580 }}>
          <span className="badge b-green" style={{ marginBottom: 12 }}>✓ Registro gratuito</span>
          <h1 style={{ fontFamily: "var(--fd)", fontSize: "clamp(22px,4vw,32px)", fontWeight: 700, color: "var(--navy)", marginBottom: 8 }}>Únete a TUCADI como técnico</h1>
          <p style={{ fontSize: 14, color: "var(--mid)", lineHeight: 1.7 }}>Tú defines los precios. TUCADI te trae los clientes y protege los pagos.</p>
        </div>
      </div>

      <div style={{ padding: "20px 16px 56px" }}>
        <div className="con" style={{ maxWidth: 580 }}>
          <div className="fbox" style={{ marginBottom: 20 }}>
            <p style={{ fontWeight: 700, color: "var(--navy)", marginBottom: 10, fontSize: 14 }}>📋 Modelo para el técnico:</p>
            <div className="fr"><span>Evaluación (precio que tú definas)</span><span style={{ color: "var(--green)" }}>100% tuyo</span></div>
            <div className="fr" style={{ color: "var(--amber)" }}><span>Tarifa TUCADI (siempre, la paga el cliente)</span><span>{fmt(PLATFORM_FEE_EVAL)}</span></div>
            <div className="fr"><span>Comisión TUCADI por trabajo</span><span style={{ fontWeight: 700 }}>10%</span></div>
            <div className="fr-tech"><span>Tú recibes por cada trabajo</span><span>90% · liberado en 7 días</span></div>
          </div>

          <form className="card-flat" style={{ padding: "22px 18px" }} onSubmit={e => { e.preventDefault(); setDone(true); }}>
            <div style={{ display: "flex", flexDirection: "column", gap: 16 }}>
              <div><label className="lbl">Nombre completo *</label><input className="inp" placeholder="Ej. Carlos Mendoza" required value={f.name} onChange={e => setF(p => ({ ...p, name: e.target.value }))} /></div>
              <div><label className="lbl">Nombre del negocio</label><input className="inp" placeholder="Opcional" value={f.business} onChange={e => setF(p => ({ ...p, business: e.target.value }))} /></div>
              <div><label className="lbl">WhatsApp / Teléfono *</label><input className="inp" placeholder="662-XXX-XXXX" required type="tel" value={f.phone} onChange={e => setF(p => ({ ...p, phone: e.target.value }))} /></div>
              <div>
                <label className="lbl">Precio de evaluación que cobrarás</label>
                <div style={{ position: "relative" }}>
                  <span style={{ position: "absolute", left: 14, top: "50%", transform: "translateY(-50%)", color: "var(--muted)" }}>$</span>
                  <input className="inp" style={{ paddingLeft: 28 }} type="number" min="0" placeholder="0 si es gratis" value={f.evalPrice} onChange={e => setF(p => ({ ...p, evalPrice: e.target.value }))} />
                </div>
                {<p style={{ fontSize: 12, color: "var(--amber)", marginTop: 6 }}>El cliente siempre paga +{fmt(PLATFORM_FEE_EVAL)} de tarifa TUCADI encima de tu precio. Ese monto no te corresponde a ti.</p>}
              </div>
              <div>
                <label className="lbl">Años de experiencia *</label>
                <select className="sel" required value={f.experience} onChange={e => setF(p => ({ ...p, experience: e.target.value }))}>
                  <option value="">Selecciona...</option>
                  {["1 año","2–3 años","4–6 años","7–10 años","Más de 10 años"].map(o => <option key={o}>{o}</option>)}
                </select>
              </div>
              <div>
                <label className="lbl">Servicios que ofreces *</label>
                <div style={{ display: "flex", gap: 10, flexWrap: "wrap", marginTop: 8 }}>
                  {svcs.map(s => (
                    <button key={s} type="button" className="btn" style={{ padding: "10px 18px", fontSize: 14, borderRadius: "var(--rs)", border: "1.5px solid", borderColor: f.services.includes(s) ? "var(--navy)" : "var(--border)", background: f.services.includes(s) ? "var(--navy)" : "white", color: f.services.includes(s) ? "white" : "var(--mid)" }} onClick={() => tog(s)}>{s}</button>
                  ))}
                </div>
              </div>
              <div>
                <label className="lbl">Zona de cobertura *</label>
                <select className="sel" required value={f.zone} onChange={e => setF(p => ({ ...p, zone: e.target.value }))}>
                  <option value="">Selecciona tu zona...</option>
                  {["Centro / Pitic","Villa del Real / Perisur","Lomas de Hermosillo / Bugambilias","San Benito / Proyecto Río","Colonia Prados / Bachoco","Periférico / Solidaridad","Toda la ciudad"].map(o => <option key={o}>{o}</option>)}
                </select>
              </div>
              <div><label className="lbl">Cuéntanos sobre tu trabajo</label><textarea className="inp" placeholder="Marcas que manejas, tus especialidades, garantías que ofreces..." value={f.description} onChange={e => setF(p => ({ ...p, description: e.target.value }))} /></div>
              <button type="submit" className="btn btn-navy full" style={{ padding: "14px", fontSize: 15 }}>Enviar solicitud →</button>
              <p style={{ fontSize: 12, color: "var(--muted)", textAlign: "center" }}>Registro gratuito. Te contactamos para activar tu perfil.</p>
            </div>
          </form>
        </div>
      </div>
    </div>
  );
}

// ─── APP ──────────────────────────────────────────────────────────────────────
export default function App() {
  const [page, setPage] = useState("home");
  const [eid, setEid] = useState(null);

  const nav = (target, id = null) => {
    setPage(target);
    if (id !== null) setEid(id);
    window.scrollTo({ top: 0, behavior: "smooth" });
  };

  return (
    <>
      <style>{G}</style>
      <div style={{ minHeight: "100vh", display: "flex", flexDirection: "column" }}>
        <Nav nav={nav} />
        <main style={{ flex: 1 }}>
          {page === "home"    && <HomePage nav={nav} />}
          {page === "how"     && <HowPage nav={nav} />}
          {page === "list"    && <ListPage nav={nav} />}
          {page === "profile" && <ProfilePage techId={eid} nav={nav} />}
          {page === "eval"    && <EvalPage techId={eid} nav={nav} />}
          {page === "signup"  && <SignupPage />}
        </main>
        <Footer nav={nav} />
      </div>
    </>
  );
}
