<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>JM Productos — Ventas</title>
<link href="https://fonts.googleapis.com/css2?family=DM+Serif+Display&family=DM+Sans:wght@300;400;500;600&family=JetBrains+Mono:wght@400;600&display=swap" rel="stylesheet">
<style>
:root{
  --jm-900:#0D1F0D;--jm-800:#1A2E1A;--jm-700:#27421A;--jm-600:#3B6D3B;
  --jm-400:#2ECC71;--jm-200:#7ECF9A;--jm-100:#C0F5D0;--jm-50:#EAF8EF;
  --surface:#F7F6F2;--card:#FFFFFF;--text:#1A1A18;--muted:#6B6B67;
  --border:rgba(0,0,0,0.09);--amber:#EF9F27;--red:#E24B4A;--blue:#378ADD;
}
*{box-sizing:border-box;margin:0;padding:0}
body{font-family:'DM Sans',sans-serif;background:var(--surface);color:var(--text);min-height:100vh}

/* TOPBAR */
.topbar{background:var(--jm-800);padding:0 20px;height:54px;display:flex;align-items:center;justify-content:space-between;position:sticky;top:0;z-index:100}
.brand{display:flex;align-items:center;gap:10px;text-decoration:none}
.brand-icon{width:32px;height:32px;background:var(--jm-400);border-radius:7px;display:flex;align-items:center;justify-content:center;font-family:'DM Serif Display',serif;font-size:13px;color:var(--jm-900);flex-shrink:0}
.brand-text h1{font-family:'DM Serif Display',serif;font-size:16px;color:#fff;font-weight:400}
.brand-text p{font-size:10px;color:var(--jm-200);letter-spacing:.06em}
.topbar-tabs{display:flex;gap:4px}
.ttab{padding:5px 14px;border-radius:20px;border:1px solid rgba(255,255,255,.12);background:transparent;color:rgba(255,255,255,.55);font-size:12px;font-family:'DM Sans',sans-serif;cursor:pointer;transition:all .15s}
.ttab.active{background:var(--jm-400);color:var(--jm-900);border-color:transparent;font-weight:500}
.ttab:hover:not(.active){background:rgba(255,255,255,.08);color:#fff}

/* LAYOUT */
.wrap{max-width:1020px;margin:0 auto;padding:18px 18px 60px}

/* METRICS */
.metrics{display:grid;grid-template-columns:repeat(4,1fr);gap:10px;margin-bottom:18px}
.mc{background:var(--card);border-radius:10px;border:1px solid var(--border);padding:13px 16px;position:relative;overflow:hidden}
.mc::after{content:'';position:absolute;top:0;right:0;width:3px;height:100%;border-radius:0 10px 10px 0}
.mc.gr::after{background:var(--jm-400)}.mc.am::after{background:var(--amber)}.mc.bl::after{background:var(--blue)}.mc.re::after{background:var(--red)}
.mc-label{font-size:10.5px;color:var(--muted);font-weight:500;letter-spacing:.03em;text-transform:uppercase;margin-bottom:5px}
.mc-val{font-family:'DM Serif Display',serif;font-size:24px;color:var(--text);line-height:1;margin-bottom:3px}
.mc-sub{font-size:11px;color:var(--muted)}

/* PANES */
.pane{display:none;animation:fi .2s ease}.pane.active{display:block}
@keyframes fi{from{opacity:0;transform:translateY(3px)}to{opacity:1;transform:none}}

/* CARDS */
.card{background:var(--card);border-radius:12px;border:1px solid var(--border);padding:18px 20px;margin-bottom:14px}
.card:last-child{margin-bottom:0}
.card-hdr{display:flex;align-items:center;justify-content:space-between;margin-bottom:14px}
.card-title{font-size:13px;font-weight:600;color:var(--text)}
.card-sub{font-size:11px;color:var(--muted)}

/* FORM */
.form-grid{display:grid;grid-template-columns:1fr 1fr;gap:12px}
.f-full{grid-column:1/-1}
.field{display:flex;flex-direction:column;gap:5px}
.field label{font-size:11.5px;font-weight:500;color:var(--muted)}
.field input,.field select,.field textarea{
  padding:9px 12px;border:1px solid var(--border);border-radius:8px;
  font-size:13px;font-family:'DM Sans',sans-serif;background:var(--surface);
  color:var(--text);outline:none;transition:border-color .15s;width:100%
}
.field input:focus,.field select:focus{border-color:var(--jm-400);background:var(--card)}

/* BTNS */
.btn{display:inline-flex;align-items:center;gap:6px;padding:9px 18px;border-radius:8px;font-size:13px;font-weight:500;cursor:pointer;transition:all .15s;border:1px solid var(--border);background:var(--card);color:var(--text);font-family:'DM Sans',sans-serif}
.btn:hover{background:var(--surface)}.btn:active{transform:scale(.98)}
.btn-primary{background:var(--jm-800);color:var(--jm-400);border-color:transparent}
.btn-primary:hover{background:var(--jm-700)}
.btn-green{background:var(--jm-400);color:var(--jm-900);border-color:transparent;font-weight:600}
.btn-green:hover{background:var(--jm-100);color:var(--jm-800)}

/* TABLE */
.tbl-wrap{border-radius:10px;border:1px solid var(--border);overflow:hidden}
table{width:100%;border-collapse:collapse;font-size:13px;background:var(--card)}
thead th{text-align:left;padding:9px 14px;font-size:11px;font-weight:600;color:var(--muted);letter-spacing:.06em;text-transform:uppercase;border-bottom:1px solid var(--border);background:var(--surface);white-space:nowrap}
tbody td{padding:10px 14px;border-bottom:1px solid var(--border);color:var(--text);vertical-align:middle}
tbody tr:last-child td{border-bottom:none}
tbody tr:hover td{background:var(--surface)}

/* BADGE */
.badge{display:inline-flex;align-items:center;font-size:11px;font-weight:600;padding:2px 9px;border-radius:20px}
.b-green{background:#dcfce7;color:#166534}.b-amber{background:#fef3c7;color:#92400e}
.b-red{background:#fee2e2;color:#991b1b}.b-blue{background:#dbeafe;color:#1e40af}
.b-gray{background:#f3f4f6;color:#374151}

/* CUOTA PREVIEW */
.cuota-preview{background:var(--jm-50);border:1px solid rgba(46,204,113,.3);border-radius:10px;padding:14px 16px;margin-top:12px}
.cp-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:10px;text-align:center}
.cp-val{font-family:'DM Serif Display',serif;font-size:22px;color:var(--jm-800)}
.cp-label{font-size:11px;color:var(--jm-600);margin-top:2px}

/* ACTION BAR */
.abar{display:flex;align-items:center;gap:10px;margin-bottom:16px;flex-wrap:wrap}
.search-wrap{position:relative;flex:1;min-width:180px}
.search-wrap input{width:100%;padding:9px 12px 9px 34px;border:1px solid var(--border);border-radius:8px;font-size:13px;font-family:'DM Sans',sans-serif;background:var(--card);color:var(--text);outline:none;transition:border-color .15s}
.search-wrap input:focus{border-color:var(--jm-400)}
.search-ic{position:absolute;left:10px;top:50%;transform:translateY(-50%);color:var(--muted);pointer-events:none}
select.flt{padding:9px 12px;border:1px solid var(--border);border-radius:8px;font-size:13px;font-family:'DM Sans',sans-serif;background:var(--card);color:var(--text);outline:none;cursor:pointer}

/* TOAST */
.toast{position:fixed;bottom:24px;left:50%;transform:translateX(-50%) translateY(10px);background:var(--jm-800);color:#fff;padding:10px 20px;border-radius:20px;font-size:13px;opacity:0;transition:all .3s;pointer-events:none;z-index:999;white-space:nowrap}
.toast.show{opacity:1;transform:translateX(-50%) translateY(0)}

/* MODAL OVERLAY */
.modal-bg{display:none;position:fixed;inset:0;background:rgba(0,0,0,.55);z-index:200;align-items:center;justify-content:center;padding:16px}
.modal-bg.open{display:flex}
.modal{background:var(--card);border-radius:16px;width:100%;max-width:640px;max-height:92vh;overflow-y:auto;animation:mup .25s ease}
@keyframes mup{from{opacity:0;transform:scale(.97)}to{opacity:1;transform:none}}
.modal-hdr{padding:18px 20px 0;display:flex;align-items:center;justify-content:space-between}
.modal-title{font-family:'DM Serif Display',serif;font-size:18px}
.modal-close{background:none;border:none;cursor:pointer;font-size:20px;color:var(--muted);padding:4px;line-height:1}
.modal-body{padding:16px 20px 20px}

/* ══════════════════════════════════════════
   CONTRATO IMPRIMIBLE
══════════════════════════════════════════ */
#contrato-print{display:none}

@media print{
  @page{
    size: A4;
    margin: 12mm 14mm;
  }
  body *{visibility:hidden!important}
  #contrato-print,#contrato-print *{visibility:visible!important}
  #contrato-print{
    display:block!important;
    position:fixed;inset:0;
    padding:0;
    background:#fff;
    font-family:'DM Sans',sans-serif;
    color:#000;
    font-size:14px !important;
  }
  #contrato-print .print-preview{
    padding:0;
    border:none;
    border-radius:0;
    font-size:14px !important;
  }
  #contrato-print .print-row{font-size:14px !important}
  #contrato-print .print-section-title{font-size:12px !important}
  #contrato-print .print-cuotas td{font-size:13px !important;padding:7px 10px}
  #contrato-print .print-cuotas th{font-size:12px !important;padding:8px 10px}
  #contrato-print .print-brand-name{font-size:20px !important}
  #contrato-print .print-meta{font-size:13px !important}
  #contrato-print .print-total-box .t-val{font-size:28px !important}
  #contrato-print .print-condiciones{font-size:12px !important}
  #contrato-print .firma-label{font-size:13px !important}
  #contrato-print .print-footer{font-size:12px !important}
}

.print-preview{font-family:'DM Sans',sans-serif;color:#111;padding:16px;border:1px solid var(--border);border-radius:10px;background:#fff;font-size:12px}
.print-header{display:flex;align-items:flex-start;justify-content:space-between;margin-bottom:10px;padding-bottom:8px;border-bottom:2px solid #1A2E1A}
.print-logo{display:flex;align-items:center;gap:8px}
.print-logo-icon{width:32px;height:32px;background:#1A2E1A;border-radius:6px;display:flex;align-items:center;justify-content:center;color:#2ECC71;font-family:'DM Serif Display',serif;font-size:13px;flex-shrink:0}
.print-brand-name{font-family:'DM Serif Display',serif;font-size:15px;color:#1A2E1A}
.print-brand-tag{font-size:9px;color:#3B6D3B;letter-spacing:.05em}
.print-meta{text-align:right;font-size:10px;color:#555}
.print-meta strong{color:#111;font-size:12px}

.print-section{margin-bottom:8px}
.print-section-title{font-size:9px;font-weight:700;color:#3B6D3B;letter-spacing:.08em;text-transform:uppercase;margin-bottom:4px;padding-bottom:3px;border-bottom:1px solid #e5e5e5}

.print-row{display:flex;justify-content:space-between;align-items:baseline;padding:2px 0;font-size:12px;border-bottom:1px dashed #f0f0f0}
.print-row:last-child{border-bottom:none}
.print-row .lbl{color:#555}
.print-row .val{font-weight:600;color:#111}

.print-cuotas{width:100%;border-collapse:collapse;margin-top:4px;font-size:11px}
.print-cuotas th{background:#1A2E1A;color:#2ECC71;padding:4px 8px;text-align:left;font-weight:700;letter-spacing:.04em;font-size:10px}
.print-cuotas td{padding:3px 8px;border-bottom:1px solid #f0f0f0;color:#111;font-size:11px}
.print-cuotas tr:nth-child(even) td{background:#f8f8f8}

.print-total-box{background:#1A2E1A;color:#fff;border-radius:6px;padding:8px 14px;margin:8px 0;display:flex;justify-content:space-between;align-items:center}
.print-total-box .t-label{font-size:11px;color:#7ECF9A}
.print-total-box .t-val{font-family:'DM Serif Display',serif;font-size:22px;color:#2ECC71}

.print-firma{display:grid;grid-template-columns:1fr 1fr;gap:20px;margin-top:14px}
.firma-box{border-top:1.5px solid #111;padding-top:5px;text-align:center}
.firma-label{font-size:10px;color:#555}

.print-footer{margin-top:10px;padding-top:8px;border-top:1px solid #e5e5e5;display:flex;justify-content:space-between;font-size:9px;color:#888}

.print-condiciones{background:#f7f6f2;border-radius:5px;padding:7px 10px;margin-top:6px;font-size:9px;color:#555;line-height:1.5}
.print-condiciones strong{color:#1A2E1A}

/* PROG BAR */
.prog{height:4px;border-radius:2px;background:#e5e5e5;overflow:hidden;margin-top:6px}
.prog-f{height:100%;border-radius:2px;background:var(--jm-400)}

/* INV ITEM CARD */
.inv-card{background:var(--card);border:1px solid var(--border);border-radius:10px;padding:14px 16px;display:flex;align-items:center;gap:14px;cursor:pointer;transition:all .15s}
.inv-card:hover{border-color:var(--jm-400);background:var(--jm-50)}
.inv-card.selected{border-color:var(--jm-400);background:var(--jm-50);box-shadow:0 0 0 2px rgba(46,204,113,.2)}
.inv-cat-icon{width:38px;height:38px;border-radius:8px;background:var(--jm-50);border:1px solid rgba(46,204,113,.2);display:flex;align-items:center;justify-content:center;font-size:18px;flex-shrink:0}
.inv-info{flex:1;min-width:0}
.inv-name{font-size:13.5px;font-weight:500;color:var(--text)}
.inv-brand{font-size:11px;color:var(--muted);margin-top:1px}
.inv-right{text-align:right}
.inv-price{font-family:'DM Serif Display',serif;font-size:17px;color:var(--text)}
.inv-cuota{font-size:11px;color:var(--muted);font-family:'JetBrains Mono',monospace}
.inv-stock{font-size:11px;margin-top:4px}

/* GRID DE PRODUCTOS */
.prod-grid{display:grid;grid-template-columns:1fr 1fr;gap:10px;margin-bottom:14px}

@media(max-width:600px){
  .metrics{grid-template-columns:1fr 1fr}
  .form-grid{grid-template-columns:1fr}
  .f-full{grid-column:1}
  .cp-grid{grid-template-columns:1fr 1fr 1fr}
  .prod-grid{grid-template-columns:1fr}
  .print-firma{grid-template-columns:1fr}
  .print-cuotas{font-size:10px}
}
</style>
</head>
<body>

<!-- TOPBAR -->
<header class="topbar">
  <div class="brand">
    <div class="brand-icon">JM</div>
    <div class="brand-text">
      <h1>JM Productos</h1>
      <p>Ventas · Inventario</p>
    </div>
  </div>
  <div class="topbar-tabs">
    <button class="ttab active" onclick="goTab('venta',this)">Nueva venta</button>
    <button class="ttab" onclick="goTab('inventario',this)">Inventario</button>
    <button class="ttab" onclick="goTab('historial',this)">Historial</button>
  </div>
</header>

<div class="wrap">

  <!-- MÉTRICAS -->
  <div class="metrics">
    <div class="mc gr">
      <div class="mc-label">Stock total</div>
      <div class="mc-val" id="m-stock">29</div>
      <div class="mc-sub">26 productos</div>
    </div>
    <div class="mc bl">
      <div class="mc-label">Valor inventario</div>
      <div class="mc-val">$5.2M</div>
      <div class="mc-sub">a precio venta</div>
    </div>
    <div class="mc am">
      <div class="mc-label">Bajo stock</div>
      <div class="mc-val" id="m-bajo">18</div>
      <div class="mc-sub">requieren reposición</div>
    </div>
    <div class="mc gr">
      <div class="mc-label">Margen total</div>
      <div class="mc-val">$1.5M</div>
      <div class="mc-sub">29% promedio</div>
    </div>
  </div>

  <!-- ═══ NUEVA VENTA ═══ -->
  <div class="pane active" id="pane-venta">

    <div style="display:grid;grid-template-columns:1fr 380px;gap:16px;align-items:start">

      <!-- LADO IZQUIERDO: Producto + Cliente -->
      <div>
        <div class="card">
          <div class="card-hdr">
            <div>
              <div class="card-title">Seleccionar producto</div>
              <div class="card-sub">Tocá el producto para seleccionarlo</div>
            </div>
            <select class="flt" onchange="filtrarCat(this.value)" style="font-size:12px">
              <option value="">Todas</option>
              <option>Celulares</option><option>TV</option>
              <option>Electrodomésticos</option><option>Cocina</option>
              <option>Audio</option><option>Hogar</option>
            </select>
          </div>
          <div class="prod-grid" id="prod-grid"></div>
        </div>

        <div class="card">
          <div class="card-hdr"><div class="card-title">Datos del comprador</div></div>
          <div class="form-grid">
            <div class="field">
              <label>Nombre</label>
              <input type="text" id="cl-nombre" placeholder="Nombre">
            </div>
            <div class="field">
              <label>Apellido</label>
              <input type="text" id="cl-apellido" placeholder="Apellido">
            </div>
            <div class="field">
              <label>DNI / ID</label>
              <input type="text" id="cl-dni" placeholder="Número de documento">
            </div>
            <div class="field">
              <label>Teléfono</label>
              <input type="tel" id="cl-tel" placeholder="11 xxxx-xxxx">
            </div>
            <div class="field">
              <label>Dirección (opcional)</label>
              <input type="text" id="cl-dir" placeholder="Calle y número">
            </div>
            <div class="field">
              <label>Codeudor (opcional)</label>
              <input type="text" id="cl-codeudor" placeholder="Nombre del codeudor">
            </div>
          </div>
        </div>
      </div>

      <!-- LADO DERECHO: Calculadora de cuotas -->
      <div style="position:sticky;top:72px">
        <div class="card">
          <div class="card-hdr"><div class="card-title">Plan de financiamiento</div></div>

          <div id="prod-selected" style="display:none;background:var(--jm-50);border-radius:8px;padding:10px 12px;margin-bottom:14px;border:1px solid rgba(46,204,113,.25)">
            <div style="font-size:13px;font-weight:500;color:var(--jm-800)" id="prod-sel-name">—</div>
            <div style="font-size:11px;color:var(--jm-600)" id="prod-sel-marca">—</div>
          </div>

          <div style="display:none" id="prod-sel-hint" style="display:block">
            <div style="text-align:center;padding:20px;color:var(--muted);font-size:13px">Seleccioná un producto para calcular</div>
          </div>
          <div id="prod-sel-hint" style="text-align:center;padding:20px;color:var(--muted);font-size:13px">← Seleccioná un producto</div>

          <div id="calc-section" style="display:none">
            <div class="form-grid" style="grid-template-columns:1fr">
              <div class="field">
                <label>Precio de venta ($)</label>
                <input type="number" id="precio-venta" oninput="calcular()" placeholder="0">
              </div>
              <div class="field">
                <label>Entrega inicial ($)</label>
                <input type="number" id="pct-entrega" placeholder="0" oninput="calcular()">
              </div>
              <div class="field">
                <label>Monto por cuota ($)</label>
                <input type="number" id="monto-cuota" placeholder="0" oninput="calcular()">
              </div>
              <div class="field">
                <label>Cantidad de cuotas</label>
                <input type="number" id="n-cuotas" placeholder="ej: 12" min="1" oninput="calcular()">
              </div>

              <div class="field">
                <label>Primera cuota</label>
                <input type="date" id="fecha-inicio">
              </div>
            </div>

            <div class="cuota-preview">
              <div class="cp-grid">
                <div>
                  <div class="cp-val" id="r-entrega">$0</div>
                  <div class="cp-label">Entrega hoy</div>
                </div>
                <div>
                  <div class="cp-val" id="r-cuota">$0</div>
                  <div class="cp-label">Cuota semanal</div>
                </div>
                <div>
                  <div class="cp-val" id="r-total">$0</div>
                  <div class="cp-label">Total a pagar</div>
                </div>
              </div>

            </div>

            <button class="btn btn-green" style="width:100%;margin-top:14px;justify-content:center;padding:12px" onclick="generarContrato()">
              <svg width="15" height="15" viewBox="0 0 15 15" fill="none" stroke="currentColor" stroke-width="1.8" stroke-linecap="round"><path d="M2 2h11v11H2zM5 5h5M5 7.5h5M5 10h3"/></svg>
              Generar contrato e imprimir
            </button>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- ═══ INVENTARIO ═══ -->
  <div class="pane" id="pane-inventario">
    <div class="abar">
      <div class="search-wrap">
        <svg class="search-ic" width="15" height="15" viewBox="0 0 15 15" fill="none" stroke="currentColor" stroke-width="1.6" stroke-linecap="round"><circle cx="6.5" cy="6.5" r="4"/><path d="M10 10l2.5 2.5"/></svg>
        <input type="text" placeholder="Buscar producto..." oninput="filtrarInv(this.value)">
      </div>
      <select class="flt" onchange="filtrarInvCat(this.value)">
        <option value="">Todas las categorías</option>
        <option>Celulares</option><option>TV</option><option>Electrodomésticos</option>
        <option>Cocina</option><option>Audio</option><option>Hogar</option>
      </select>
      <button class="btn btn-primary" onclick="abrirEntrada()">+ Entrada de stock</button>
    </div>
    <div class="tbl-wrap">
      <table>
        <thead>
          <tr><th>Producto</th><th>Marca</th><th>Categoría</th><th>P. Venta</th><th>P. Costo</th><th>Margen</th><th>Cuota 12sem</th><th>Stock</th><th>Estado</th></tr>
        </thead>
        <tbody id="inv-tbody"></tbody>
      </table>
    </div>
  </div>

  <!-- ═══ HISTORIAL ═══ -->
  <div class="pane" id="pane-historial">
    <div id="historial-empty" style="text-align:center;padding:60px 20px;color:var(--muted)">
      <div style="font-size:40px;margin-bottom:12px;opacity:.3">📋</div>
      <div style="font-size:14px">Aún no hay ventas registradas en esta sesión.</div>
      <div style="font-size:12px;margin-top:4px">Las ventas aparecen aquí cuando generás un contrato.</div>
    </div>
    <div id="historial-list" style="display:none">
      <div class="tbl-wrap">
        <table>
          <thead><tr><th>#</th><th>Fecha</th><th>Cliente</th><th>Producto</th><th>Entrega</th><th>Cuota</th><th>Total</th><th>Acción</th></tr></thead>
          <tbody id="hist-tbody"></tbody>
        </table>
      </div>
    </div>
  </div>

</div>

<!-- MODAL CONTRATO -->
<div class="modal-bg" id="modal-contrato">
  <div class="modal">
    <div class="modal-hdr">
      <div class="modal-title">Contrato de financiamiento</div>
      <button class="modal-close" onclick="cerrarModal('modal-contrato')">✕</button>
    </div>
    <div class="modal-body">
      <div class="print-preview" id="contrato-preview"></div>
      <div style="display:flex;gap:10px;margin-top:16px;justify-content:flex-end;flex-wrap:wrap">
        <button class="btn" onclick="cerrarModal('modal-contrato')">Cerrar</button>
        <button class="btn" onclick="compartirWsp()" style="background:#25D366;color:#fff;border-color:transparent;font-weight:600">
          <svg width="14" height="14" viewBox="0 0 14 14" fill="currentColor"><path d="M7 0C3.13 0 0 3.13 0 7c0 1.23.33 2.4.9 3.4L0 14l3.7-.96A7 7 0 107 0zm0 12.73a5.73 5.73 0 01-2.92-.8l-.21-.12-2.2.57.59-2.14-.13-.22A5.73 5.73 0 117 12.73zm3.14-4.28c-.17-.09-.99-.49-1.14-.54-.15-.06-.26-.09-.37.09-.11.17-.43.54-.52.65-.1.11-.19.12-.36.04-.17-.09-.72-.27-1.37-.85a5.1 5.1 0 01-.95-1.18c-.1-.17-.01-.27.08-.35.08-.08.17-.2.26-.3.09-.1.12-.17.17-.28.06-.11.03-.21-.01-.3-.05-.09-.37-.9-.51-1.23-.13-.32-.27-.27-.37-.28h-.32c-.11 0-.29.04-.44.21-.15.17-.58.57-.58 1.38s.6 1.6.68 1.71c.09.11 1.17 1.79 2.84 2.51.4.17.71.27.95.35.4.13.76.11 1.05.07.32-.05.99-.4 1.13-.8.14-.38.14-.71.1-.78-.05-.07-.16-.11-.33-.2z"/></svg>
          Enviar por WhatsApp
        </button>
      </div>
    </div>
  </div>
</div>

<!-- MODAL ENTRADA STOCK -->
<div class="modal-bg" id="modal-entrada">
  <div class="modal">
    <div class="modal-hdr">
      <div class="modal-title">Agregar producto al inventario</div>
      <button class="modal-close" onclick="cerrarModal('modal-entrada')">✕</button>
    </div>
    <div class="modal-body">
      <div class="form-grid">
        <div class="field f-full">
          <label>Producto existente (o dejá vacío para nuevo)</label>
          <select id="ent-prod" onchange="checkNuevoProd()">
            <option value="">— Producto nuevo —</option>
          </select>
        </div>
        <div id="campos-nuevo">
          <div class="form-grid">
            <div class="field">
              <label>Nombre del producto</label>
              <input type="text" id="ent-nombre" placeholder="Ej: Samsung Galaxy A16">
            </div>
            <div class="field">
              <label>Marca</label>
              <input type="text" id="ent-marca" placeholder="Ej: Samsung">
            </div>
            <div class="field f-full">
              <label>Categoría</label>
              <select id="ent-cat">
                <option>Celulares</option><option>TV</option>
                <option>Electrodomésticos</option><option>Cocina</option>
                <option>Audio</option><option>Hogar</option>
              </select>
            </div>
          </div>
        </div>
        <div class="field">
          <label>Cantidad</label>
          <input type="number" id="ent-cant" value="1" min="1">
        </div>
        <div class="field">
          <label>Precio de costo ($)</label>
          <input type="number" id="ent-costo" placeholder="0">
        </div>
        <div class="field">
          <label>Precio de venta ($)</label>
          <input type="number" id="ent-venta" placeholder="0">
        </div>
        <div class="field f-full">
          <label>Nota (opcional)</label>
          <input type="text" id="ent-nota" placeholder="Proveedor, condición, etc.">
        </div>
      </div>
      <div style="display:flex;gap:10px;margin-top:16px;justify-content:flex-end">
        <button class="btn" onclick="cerrarModal('modal-entrada')">Cancelar</button>
        <button class="btn btn-primary" onclick="guardarEntrada()">Confirmar entrada</button>
      </div>
    </div>
  </div>
</div>

<!-- CONTRATO PARA IMPRIMIR -->
<div id="contrato-print"></div>

<div class="toast" id="toast"></div>

<script>
// ═══════════════════════════════════════════
// DATOS
// ═══════════════════════════════════════════
const catIcons = {
  'Celulares':'📱','TV':'📺','Electrodomésticos':'🔌','Cocina':'🍳','Audio':'🔊','Hogar':'🏠'
};

let productos = [];

let selectedProd = null;
let ventas = [];
let vNum = 1;

// ═══════════════════════════════════════════
// NAVEGACIÓN
// ═══════════════════════════════════════════
function goTab(id, btn) {
  document.querySelectorAll('.ttab').forEach(b => b.classList.remove('active'));
  document.querySelectorAll('.pane').forEach(p => p.classList.remove('active'));
  if(btn) btn.classList.add('active');
  document.getElementById('pane-' + id).classList.add('active');
}

// ═══════════════════════════════════════════
// RENDER PRODUCTOS
// ═══════════════════════════════════════════
function renderProds(data) {
  const grid = document.getElementById('prod-grid');
  if (!data.length) {
    grid.innerHTML = `<div style="grid-column:1/-1;text-align:center;padding:40px 20px;color:var(--muted)">
      <div style="font-size:32px;margin-bottom:8px;opacity:.3">📦</div>
      <div style="font-size:13px">No hay productos en el inventario</div>
      <div style="font-size:12px;margin-top:4px">Andá a <b>Inventario</b> → <b>+ Entrada de stock</b> para agregar</div>
    </div>`;
    return;
  }
  document.getElementById('prod-grid').innerHTML = data.map(p => {
    const cuota = calcCuota(p.venta * 0.8, 12, 2.5);
    const sel = selectedProd && selectedProd.id === p.id;
    const stockOk = p.stock > 0;
    return `<div class="inv-card ${sel ? 'selected' : ''} ${!stockOk ? 'disabled' : ''}" 
      onclick="${stockOk ? `selProd(${p.id})` : 'showToast(\"Sin stock\")'}" 
      style="${!stockOk ? 'opacity:.45;cursor:not-allowed' : ''}">
      <div class="inv-cat-icon">${catIcons[p.cat] || '📦'}</div>
      <div class="inv-info">
        <div class="inv-name">${p.nombre}</div>
        <div class="inv-brand">${p.marca} · ${p.cat}</div>
      </div>
      <div class="inv-right">
        <div class="inv-price">${fmt(p.venta)}</div>
        <div class="inv-cuota">${fmt(cuota)}/sem</div>
        <div class="inv-stock"><span class="badge ${p.stock > 1 ? 'b-green' : p.stock === 1 ? 'b-amber' : 'b-red'}">${p.stock} en stock</span></div>
      </div>
    </div>`;
  }).join('');
}

function filtrarCat(cat) {
  renderProds(cat ? productos.filter(p => p.cat === cat) : productos);
}

renderProds(productos);

// ═══════════════════════════════════════════
// SELECCIONAR PRODUCTO
// ═══════════════════════════════════════════
function selProd(id) {
  selectedProd = productos.find(p => p.id === id);
  renderProds(document.querySelector('.flt') ? 
    (document.querySelectorAll('.flt')[0].value ? 
      productos.filter(p => p.cat === document.querySelectorAll('.flt')[0].value) : productos) : productos);

  document.getElementById('prod-selected').style.display = 'block';
  document.getElementById('prod-sel-hint').style.display = 'none';
  document.getElementById('calc-section').style.display = 'block';
  document.getElementById('prod-sel-name').textContent = selectedProd.nombre;
  document.getElementById('prod-sel-marca').textContent = selectedProd.marca + ' · ' + selectedProd.cat;
  document.getElementById('precio-venta').value = selectedProd.venta;
  document.getElementById('pct-entrega').value = '';
  document.getElementById('monto-cuota').value = '';
  calcular();
}

// ═══════════════════════════════════════════
// CALCULADORA
// ═══════════════════════════════════════════
function calcCuota(capital, n, tasa) {
  const r = tasa / 100;
  if (r === 0) return Math.round(capital / n);
  return Math.round(capital * r * Math.pow(1+r, n) / (Math.pow(1+r, n) - 1));
}

function calcular() {
  const pv      = parseFloat(document.getElementById('precio-venta').value) || 0;
  const entrega = parseFloat(document.getElementById('pct-entrega').value) || 0;
  const cuota   = parseFloat(document.getElementById('monto-cuota').value) || 0;
  const n       = parseInt(document.getElementById('n-cuotas').value) || 0;
  const resto   = Math.max(0, pv - entrega);
  const total   = entrega + cuota * n;
  document.getElementById('r-entrega').textContent = fmt(entrega);
  document.getElementById('r-cuota').textContent   = fmt(cuota);
  document.getElementById('r-total').textContent   = fmt(total);
}

// ═══════════════════════════════════════════
// GENERAR CONTRATO
// ═══════════════════════════════════════════
function generarContrato() {
  if (!selectedProd) { showToast('Seleccioná un producto'); return; }
  const nombre = document.getElementById('cl-nombre').value.trim();
  const apellido = document.getElementById('cl-apellido').value.trim();
  if (!nombre || !apellido) { showToast('Completá nombre y apellido del cliente'); return; }

  const dni = document.getElementById('cl-dni').value.trim();
  const tel = document.getElementById('cl-tel').value.trim();
  const dir = document.getElementById('cl-dir').value.trim();
  const codeudor = document.getElementById('cl-codeudor').value.trim();
  const pv      = parseFloat(document.getElementById('precio-venta').value) || selectedProd.venta;
  const entrega = parseFloat(document.getElementById('pct-entrega').value) || 0;
  const cuota   = parseFloat(document.getElementById('monto-cuota').value) || 0;
  const n       = parseInt(document.getElementById('n-cuotas').value) || 0;
  const resto   = Math.max(0, pv - entrega);
  const total   = entrega + cuota * n;

  // Fecha inicio cuotas
  const hoy = new Date();
  const fechaInicio = document.getElementById('fecha-inicio').value
    ? new Date(document.getElementById('fecha-inicio').value + 'T00:00:00')
    : new Date(hoy.getTime() + 7 * 24 * 60 * 60 * 1000);

  // Generar tabla de cuotas
  const cuotasRows = Array.from({ length: n }, (_, i) => {
    const d = new Date(fechaInicio.getTime() + i * 7 * 24 * 60 * 60 * 1000);
    const ds = d.toLocaleDateString('es-AR', { day: '2-digit', month: '2-digit', year: 'numeric' });
    return `<tr>
      <td style="font-family:'JetBrains Mono',monospace;font-size:11px;color:#666">${String(i+1).padStart(2,'0')}</td>
      <td>${ds}</td>
      <td style="font-weight:600;font-size:13px">${fmt(cuota)}</td>
      <td style="width:80px;border-bottom:1px dashed #bbb">&nbsp;</td>
    </tr>`;
  }).join('');

  const contratoNum = String(vNum).padStart(4, '0');
  const fechaHoy = hoy.toLocaleDateString('es-AR', { day: '2-digit', month: '2-digit', year: 'numeric' });

  const html = `
    <div class="print-header">
      <div class="print-logo">
        <div class="print-logo-icon">JM</div>
        <div>
          <div class="print-brand-name">JM Productos</div>
          <div class="print-brand-tag">VENTAS DIRECTAS · PAGOS SEMANALES</div>
        </div>
      </div>
      <div class="print-meta">
        <div><strong>Contrato N° ${contratoNum}</strong></div>
        <div>Fecha: ${fechaHoy}</div>
        <div>WhatsApp: +54 9 11 5389-3728</div>

      </div>
    </div>

    <div class="print-section">
      <div class="print-section-title">Datos del comprador</div>
      <div class="print-row"><span class="lbl">Nombre completo</span><span class="val">${nombre} ${apellido}</span></div>
      <div class="print-row"><span class="lbl">DNI / Documento</span><span class="val">${dni || '—'}</span></div>
      <div class="print-row"><span class="lbl">Teléfono</span><span class="val">${tel || '—'}</span></div>
      ${dir ? `<div class="print-row"><span class="lbl">Dirección</span><span class="val">${dir}</span></div>` : ''}
      ${codeudor ? `<div class="print-row"><span class="lbl">Codeudor</span><span class="val">${codeudor}</span></div>` : ''}
    </div>

    <div class="print-section">
      <div class="print-section-title">Producto financiado</div>
      <div class="print-row"><span class="lbl">Producto</span><span class="val">${selectedProd.nombre}</span></div>
      <div class="print-row"><span class="lbl">Marca</span><span class="val">${selectedProd.marca}</span></div>
      <div class="print-row"><span class="lbl">Categoría</span><span class="val">${selectedProd.cat}</span></div>
      <div class="print-row"><span class="lbl">Precio de venta</span><span class="val">${fmt(pv)}</span></div>
    </div>

    <div class="print-section">
      <div class="print-section-title">Plan de financiamiento</div>
      <div class="print-row"><span class="lbl">Entrega inicial</span><span class="val" style="color:#1A2E1A;font-size:14px">${fmt(entrega)}</span></div>
      <div class="print-row"><span class="lbl">Capital financiado</span><span class="val">${fmt(resto)}</span></div>
      <div class="print-row"><span class="lbl">Cantidad de cuotas</span><span class="val">${n} cuotas semanales</span></div>
      <div class="print-row"><span class="lbl">Cuota semanal</span><span class="val" style="color:#1A2E1A;font-size:14px">${fmt(cuota)}</span></div>
    </div>

    <div class="print-total-box">
      <div>
        <div class="t-label">Total a pagar (entrega + cuotas)</div>
        <div style="font-size:11px;color:#7ECF9A;margin-top:2px">Interés total: ${fmt(total - pv)}</div>
      </div>
      <div class="t-val">${fmt(total)}</div>
    </div>

    <div class="print-section">
      <div class="print-section-title">Calendario de cuotas</div>
      <table class="print-cuotas">
        <thead>
          <tr><th>N°</th><th>Fecha vencimiento</th><th>Monto cuota</th><th>Firma / Sello</th></tr>
        </thead>
        <tbody>${cuotasRows}</tbody>
      </table>
    </div>

    <div class="print-condiciones">
      <strong>Condiciones del acuerdo:</strong> El comprador se compromete a abonar las cuotas semanales en las fechas indicadas. 
      El atraso en el pago generará un recargo del <strong>10% por día de mora</strong> sobre la cuota vencida. 
      El pago se realiza por transferencia bancaria o en efectivo en el local según se acuerde. 
      Este documento es válido como comprobante de la operación.
    </div>

    <div class="print-firma">
      <div class="firma-box">
        <div class="firma-label">Firma del comprador — ${nombre} ${apellido}</div>
        ${dni ? `<div class="firma-label" style="margin-top:4px">DNI: ${dni}</div>` : ''}
      </div>
      <div class="firma-box">
        <div class="firma-label">Firma del vendedor — JM Productos</div>
        <div class="firma-label" style="margin-top:4px">+54 9 11 5389-3728</div>
      </div>
    </div>

    <div class="print-footer">
      <span>JM Productos · Ventas directas · Pagos semanales</span>
      <span>Contrato N° ${contratoNum} — ${fechaHoy}</span>
    </div>`;

  document.getElementById('contrato-preview').innerHTML = html;
  document.getElementById('contrato-print').innerHTML = `<div class="print-preview">${html}</div>`;
  document.getElementById('modal-contrato').classList.add('open');

  // Guardar datos del contrato para los botones del modal
  window._contratoActual = {
    nombre, apellido, tel,
    producto: selectedProd.nombre,
    entrega: fmt(entrega),
    cuota: fmt(cuota),
    total: fmt(total),
    n: n,
    fechaHoy,
    htmlContrato: html
  };

  // Registrar venta y descontar stock
  ventas.unshift({
    num: contratoNum, fecha: fechaHoy,
    cliente: `${nombre} ${apellido}`,
    producto: selectedProd.nombre,
    entrega: fmt(entrega), cuota: fmt(cuota), total: fmt(total),
    contratoHtml: html
  });
  vNum++;

  // Descontar stock
  const prod = productos.find(p => p.id === selectedProd.id);
  if (prod) {
    prod.stock = Math.max(0, prod.stock - 1);
    renderProds(productos);
    renderInv(productos);
    actualizarMetricas();
    if (prod.stock === 0) {
      showToast(`${prod.nombre} — sin stock`);
    }
  }

  renderHistorial();
}

function compartirWsp() {
  const data = window._contratoActual;
  if (!data) { showToast('Primero generá el contrato'); return; }

  const nombreArchivo = `JM_${data.nombre}_${data.apellido}_${data.fechaHoy.replace(/\//g,'-')}`.replace(/\s+/g,'_') + '.pdf';

  // 1. Quitar restricciones del modal temporalmente
  const modal = document.querySelector('#modal-contrato .modal');
  const el = document.getElementById('contrato-preview');
  
  const origModalMaxH = modal.style.maxHeight;
  const origModalOverflow = modal.style.overflow;
  const origElBorder = el.style.border;
  const origElRadius = el.style.borderRadius;
  
  modal.style.maxHeight = 'none';
  modal.style.overflow = 'visible';
  el.style.border = 'none';
  el.style.borderRadius = '0';

  // 2. Scroll al tope del modal
  modal.scrollTop = 0;

  // 3. Capturar y descargar
  setTimeout(() => {
    html2pdf().set({
      margin: [8, 10, 8, 10],
      filename: nombreArchivo,
      image: { type: 'jpeg', quality: 0.95 },
      html2canvas: { 
        scale: 2, 
        useCORS: true, 
        backgroundColor: '#ffffff',
        scrollY: 0,
        scrollX: 0
      },
      jsPDF: { unit: 'mm', format: 'a4', orientation: 'portrait' },
      pagebreak: { mode: 'avoid-all' }
    }).from(el).save().then(() => {
      // 4. Restaurar modal
      modal.style.maxHeight = origModalMaxH;
      modal.style.overflow = origModalOverflow;
      el.style.border = origElBorder;
      el.style.borderRadius = origElRadius;

      // 5. Abrir WhatsApp
      const telLimpio = (data.tel || '').replace(/\D/g,'');
      if (telLimpio) {
        const msg = `Hola ${data.nombre}! Te paso el comprobante de tu compra en JM Productos 📋\n\n`
          + `*Producto:* ${data.producto}\n`
          + `*Entrega inicial:* ${data.entrega}\n`
          + `*Cuota semanal:* ${data.cuota} x ${data.n} semanas\n`
          + `*Total a pagar:* ${data.total}\n\n`
          + `📎 Adjunto el contrato en PDF ✅`;
        window.open(`https://wa.me/54${telLimpio}?text=${encodeURIComponent(msg)}`, '_blank');
        showToast(`PDF descargado — abriendo chat con ${data.nombre}`);
      } else {
        showToast('PDF descargado. Cargá el teléfono para enviar por WhatsApp.');
      }
    }).catch(err => {
      modal.style.maxHeight = origModalMaxH;
      modal.style.overflow = origModalOverflow;
      el.style.border = origElBorder;
      el.style.borderRadius = origElRadius;
      console.error('Error PDF:', err);
      showToast('Error al generar PDF');
    });
  }, 300);
}

// ═══════════════════════════════════════════
// INVENTARIO TABLE
// ═══════════════════════════════════════════
function renderInv(data) {
  if (!data.length) {
    document.getElementById('inv-tbody').innerHTML = `<tr><td colspan="9" style="text-align:center;padding:40px;color:var(--muted)">
      No hay productos — tocá <b>"+ Entrada de stock"</b> para agregar el primero
    </td></tr>`;
    return;
  }
  document.getElementById('inv-tbody').innerHTML = data.map(p => {
    const margen = p.venta > 0 ? Math.round((p.venta - p.costo) / p.venta * 100) : 0;
    const cuota = calcCuota(p.venta * 0.8, 12, 2.5);
    const estado = p.stock > 1 ? 'Disponible' : p.stock === 1 ? 'Bajo stock' : 'Sin stock';
    return `<tr>
      <td style="font-weight:500">${catIcons[p.cat] || '📦'} ${p.nombre}</td>
      <td style="color:var(--muted)">${p.marca}</td>
      <td><span class="badge b-gray">${p.cat}</span></td>
      <td style="font-weight:500">${fmt(p.venta)}</td>
      <td style="color:var(--muted)">${fmt(p.costo)}</td>
      <td><span class="badge ${margen > 35 ? 'b-green' : margen > 20 ? 'b-blue' : 'b-amber'}">${margen}%</span></td>
      <td style="font-family:'JetBrains Mono',monospace;font-size:11px;color:var(--muted)">${fmt(cuota)}/sem</td>
      <td style="text-align:center;font-family:'JetBrains Mono',monospace">${p.stock}</td>
      <td><span class="badge ${p.stock > 1 ? 'b-green' : p.stock === 1 ? 'b-amber' : 'b-red'}">${estado}</span></td>
    </tr>`;
  }).join('');
}
renderInv(productos);

function filtrarInv(q) { renderInv(productos.filter(p => (p.nombre + p.marca).toLowerCase().includes(q.toLowerCase()))); }
function filtrarInvCat(c) { renderInv(c ? productos.filter(p => p.cat === c) : productos); }

// ═══════════════════════════════════════════
// HISTORIAL
// ═══════════════════════════════════════════
function renderHistorial() {
  if (!ventas.length) return;
  document.getElementById('historial-empty').style.display = 'none';
  document.getElementById('historial-list').style.display = 'block';
  document.getElementById('hist-tbody').innerHTML = ventas.map(v => `
    <tr>
      <td style="font-family:'JetBrains Mono',monospace;font-size:11px;color:var(--muted)">${v.num}</td>
      <td>${v.fecha}</td>
      <td style="font-weight:500">${v.cliente}</td>
      <td>${v.producto}</td>
      <td>${v.entrega}</td>
      <td>${v.cuota}/sem</td>
      <td style="font-weight:500">${v.total}</td>
      <td><button class="btn" style="padding:4px 10px;font-size:11px" onclick="reimprimir('${v.num}')">Reimprimir</button></td>
    </tr>`).join('');
}

function reimprimir(num) {
  const v = ventas.find(x => x.num === num);
  if (!v) return;
  document.getElementById('contrato-preview').innerHTML = v.contratoHtml;
  document.getElementById('contrato-print').innerHTML = `<div class="print-preview">${v.contratoHtml}</div>`;
  document.getElementById('modal-contrato').classList.add('open');
}

// ═══════════════════════════════════════════
// ENTRADA STOCK
// ═══════════════════════════════════════════
function abrirEntrada() {
  const sel = document.getElementById('ent-prod');
  sel.innerHTML = '<option value="">— Producto nuevo —</option>' +
    productos.map(p => `<option value="${p.id}">${p.nombre} (stock: ${p.stock})</option>`).join('');
  checkNuevoProd();
  document.getElementById('modal-entrada').classList.add('open');
}

function checkNuevoProd() {
  const sel = document.getElementById('ent-prod').value;
  document.getElementById('campos-nuevo').style.display = sel ? 'none' : 'block';
}

let nextId = 1;

function guardarEntrada() {
  const idSel = document.getElementById('ent-prod').value;
  const cant = parseInt(document.getElementById('ent-cant').value) || 1;
  const costo = parseFloat(document.getElementById('ent-costo').value) || 0;
  const venta = parseFloat(document.getElementById('ent-venta').value) || 0;

  if (idSel) {
    // Producto existente — sumar stock
    const p = productos.find(x => x.id === parseInt(idSel));
    if (!p) { showToast('Producto no encontrado'); return; }
    p.stock += cant;
    if (costo) p.costo = costo;
    if (venta) p.venta = venta;
    showToast(`+${cant} ${p.nombre} — stock: ${p.stock}`);
  } else {
    // Producto nuevo
    const nombre = document.getElementById('ent-nombre').value.trim();
    const marca = document.getElementById('ent-marca').value.trim();
    const cat = document.getElementById('ent-cat').value;
    if (!nombre) { showToast('Ingresá el nombre del producto'); return; }
    if (!venta) { showToast('Ingresá el precio de venta'); return; }
    productos.push({
      id: nextId++,
      nombre, marca: marca || '—', cat,
      venta, costo,
      stock: cant
    });
    showToast(`${nombre} agregado al inventario (${cant} unid.)`);
    // Limpiar campos
    document.getElementById('ent-nombre').value = '';
    document.getElementById('ent-marca').value = '';
  }

  renderInv(productos);
  renderProds(productos);
  actualizarMetricas();
  cerrarModal('modal-entrada');
  // Limpiar campos comunes
  document.getElementById('ent-cant').value = '1';
  document.getElementById('ent-costo').value = '';
  document.getElementById('ent-venta').value = '';
  document.getElementById('ent-nota').value = '';
}

function actualizarMetricas() {
  document.getElementById('m-stock').textContent = productos.reduce((s, p) => s + p.stock, 0);
  document.getElementById('m-bajo').textContent = productos.filter(p => p.stock <= 1).length;
}

// ═══════════════════════════════════════════
// UTILS
// ═══════════════════════════════════════════
function fmt(n) {
  return '$' + Math.round(n).toLocaleString('es-AR');
}

function cerrarModal(id) {
  document.getElementById(id).classList.remove('open');
}

document.querySelectorAll('.modal-bg').forEach(m => {
  m.addEventListener('click', e => { if (e.target === m) m.classList.remove('open'); });
});

let toastT;
function showToast(msg) {
  const t = document.getElementById('toast');
  t.textContent = msg;
  t.classList.add('show');
  clearTimeout(toastT);
  toastT = setTimeout(() => t.classList.remove('show'), 2500);
}

// Fecha default
const manana = new Date();
manana.setDate(manana.getDate() + 7);
document.getElementById('fecha-inicio').value = manana.toISOString().split('T')[0];
</script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/html2pdf.js/0.10.1/html2pdf.bundle.min.js"></script>
</body>
</html>
