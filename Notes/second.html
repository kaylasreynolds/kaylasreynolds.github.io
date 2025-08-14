<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>Client Management</title>
<style>
  :root{
    --grad1:#4c51bf; --grad2:#553c9a;
    --ok:#2f855a;--ok2:#276749;
    --danger:#c53030;--danger2:#97266d;
    --text:#222;--muted:#555;--muted2:#888;
    --card:rgba(255,255,255,.95);--ring:#d6d6d6;
    --shadow:0 10px 30px rgba(0,0,0,.12);
  }
  *{box-sizing:border-box}html,body{height:100%}
  body{margin:0;font-family:-apple-system,BlinkMacSystemFont,"Segoe UI",Inter,Roboto,Ubuntu,system-ui,sans-serif;background:linear-gradient(135deg,#667eea,#764ba2);color:var(--text)}
  .container{max-width:1200px;margin:auto;padding:20px}
  header{background:var(--card);backdrop-filter:blur(10px);border-radius:20px;padding:24px;margin-bottom:20px;box-shadow:var(--shadow)}
  h1{margin:0 0 6px;background:linear-gradient(135deg,var(--grad1),var(--grad2));-webkit-background-clip:text;background-clip:text;-webkit-text-fill-color:transparent}
  .toolbar{display:flex;gap:10px;flex-wrap:wrap;margin-top:10px}
  .tabs{display:flex;gap:10px;flex-wrap:wrap;margin:16px 0}
  .tab{padding:10px 18px;border:0;border-radius:999px;background:#ffffff;cursor:pointer;font-weight:700;box-shadow:0 4px 15px rgba(0,0,0,.1)}
  .tab.active,[aria-selected="true"]{color:#fff;background:linear-gradient(135deg,var(--grad1),var(--grad2))}
  .stats-grid{display:grid;grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));gap:20px;margin-bottom:30px;align-items:stretch}
  .card{background:var(--card);border-radius:16px;box-shadow:var(--shadow);padding:20px}
  .stat-number{font-size:2rem;font-weight:800;background:linear-gradient(135deg,var(--grad1),var(--grad2));-webkit-background-clip:text;background-clip:text;-webkit-text-fill-color:transparent}
  .muted{color:var(--muted);font-size:.95rem}
  .search{display:grid;grid-template-columns:1fr auto;gap:10px;align-items:center;margin-bottom:12px}
  .search .row{display:flex;gap:10px}
  .search input,.search select{width:100%;padding:12px 14px;border-radius:12px;border:2px solid var(--ring);font-size:1rem}
  .list{display:grid;gap:12px}
  .client-item,.interaction-item{background:#fff;border-radius:12px;padding:16px;border-left:4px solid transparent;box-shadow:0 2px 10px rgba(0,0,0,.06)}
  .client-item:hover,.interaction-item:hover{transform:translateY(-1px);transition:.2s;box-shadow:0 6px 16px rgba(0,0,0,.1);border-left-color:var(--grad1)}
  .client-header{display:flex;justify-content:space-between;gap:12px}
  .client-name{font-weight:800}
  .chip{display:inline-flex;align-items:center;gap:6px;padding:4px 10px;border-radius:999px;font-size:.75rem;font-weight:700}
  .status-introductory{background:#e6f0ff;color:#1a365d}
  .status-first-appointment{background:#fffbea;color:#744210}
  .status-established{background:#c6f6d5;color:#22543d}
  .badge-sale{background:linear-gradient(135deg,var(--ok),var(--ok2));color:#fff;padding:4px 10px;border-radius:999px;font-size:.75rem;font-weight:800;margin-left:8px}
  .buttons{display:flex;gap:8px;flex-wrap:wrap;margin-top:10px}
  .btn{padding:10px 16px;border:0;border-radius:999px;font-weight:800;cursor:pointer}
  .btn.primary{color:#fff;background:linear-gradient(135deg,var(--grad1),var(--grad2))}
  .btn.ghost{background:#e5e5e5}
  .btn.danger{color:#fff;background:linear-gradient(135deg,var(--danger),var(--danger2))}
  .tags{display:flex;flex-wrap:wrap;gap:8px;margin-top:6px}
  .tag{background:#eef;color:#333;padding:4px 10px;border-radius:999px;font-size:.75rem;font-weight:700}

  /* modal */
  .modal{position:fixed;inset:0;display:none;align-items:center;justify-content:center;background:rgba(0,0,0,.45);z-index:10}
  .modal.active{display:flex}
  .panel{background:#fff;border-radius:16px;width:min(560px,92vw);max-height:90vh;overflow:auto;padding:20px}
  .panel header{display:flex;align-items:center;justify-content:space-between;margin:0 0 10px}
  .x{background:transparent;border:0;font-size:22px;cursor:pointer;color:var(--muted2)}
  label{display:block;font-weight:700;margin:12px 0 6px}
  input,select,textarea{width:100%;padding:10px;border-radius:10px;border:2px solid var(--ring);font-size:1rem}
  textarea{min-height:90px;resize:vertical}
  .row-cols{display:grid;grid-template-columns:repeat(auto-fit,minmax(180px,1fr));gap:12px}
  .empty-state{text-align:center;color:var(--muted2);padding:28px}

  /* Follow Up: 4 columns on one line, compact (no scrollbar) */
  .followup-sections{
    display:grid;
    grid-template-columns:repeat(4, minmax(0, 1fr));
    gap:12px;
  }
  .followup-sections > div{min-width:0}
  .followup-sections h3{margin-top:0;font-size:.95rem;color:var(--muted);font-weight:700}

  /* Follow-up cards: compact + bottom buttons */
  .followup-card{
    background:#fff;border-radius:12px;box-shadow:0 2px 10px rgba(0,0,0,.06);
    border-left:4px solid transparent;padding:12px;display:flex;flex-direction:column;min-height:140px
  }
  .followup-card:hover{transform:translateY(-1px);transition:.2s;box-shadow:0 6px 16px rgba(0,0,0,.1);border-left-color:var(--grad1)}
  .followup-top{display:flex;justify-content:space-between;gap:10px}
  .followup-main{display:grid;gap:4px}
  .followup-main .client-name{font-size:.95rem}
  .followup-main .muted{font-size:.85rem}
  .followup-main div{font-size:.9rem}
  .card-actions{margin-top:auto;display:flex;gap:6px;justify-content:flex-end;flex-wrap:wrap}
  .pill-911{background:#ffe2e2;color:#7a0613;border-left-color:#c53030}

  /* Filters: make "Filter by Style" smaller */
  .filters{display:flex;flex-direction:column;gap:6px;margin:8px 0 12px}
  .filters-row{display:flex;flex-wrap:wrap;gap:6px;align-items:center}
  .filters-title{font-weight:800;margin-right:6px;font-size:.9rem}
  .chk{background:#fff;border:2px solid var(--ring);padding:4px 8px;border-radius:999px;display:flex;gap:6px;align-items:center;cursor:pointer;font-size:.85rem}
  .chk input{accent-color:#4c51bf;transform:scale(.9)}
  .filters-controls{display:flex;gap:8px;align-items:center;flex-wrap:wrap}
  .filters-controls select{padding:6px 8px;border-radius:8px;border:2px solid var(--ring);font-size:.9rem}

  @media (max-width: 900px){
    .container{padding:12px}
    .followup-main .client-name{font-size:.9rem}
    .followup-main .muted{font-size:.8rem}
  }
</style>
</head>
<body>
  <div class="container">
    <header>
      <h1>Client Management</h1>
      <div class="toolbar">
        <button id="exportBtn" class="btn ghost">â¬ï¸ Export Data</button>
        <button id="importBtn" class="btn ghost">â¬ï¸ Import Data</button>
        <input id="importFile" type="file" accept="application/json" style="display:none">
        <button id="clearBtn" class="btn danger">ðï¸ Clear Data</button>
      </div>
    </header>

    <!-- Tabs -->
    <div class="tabs" role="tablist" aria-label="Main sections">
      <button class="tab active" role="tab" aria-selected="true" data-tab="dashboard">ð Dashboard</button>
      <button class="tab" role="tab" aria-selected="false" data-tab="clients">ð¥ Clients</button>
      <button class="tab" role="tab" aria-selected="false" data-tab="interactions">ð¬ Interactions</button>
      <button class="tab" role="tab" aria-selected="false" data-tab="sales">ð° Sales</button>
      <button class="tab" role="tab" aria-selected="false" data-tab="followups">ð Follow Up</button>
    </div>

    <!-- Dashboard -->
    <div id="dashboard" class="tab-content">
      <div class="stats-grid">
        <div class="card"><div class="stat-number" id="totalClients">0</div><div class="muted">Total Clients</div></div>
        <div class="card"><div class="stat-number" id="totalInteractions">0</div><div class="muted">Total Interactions</div></div>
        <div class="card"><div class="stat-number" id="activeThisMonth">0</div><div class="muted">Active This Month</div></div>
        <div class="card"><div class="stat-number" id="totalSales">$0.00</div><div class="muted">Total Sales</div></div>
      </div>

      <div class="card" style="margin-top:20px">
        <h2 style="margin:0 0 12px">Recent Activity</h2>
        <div class="activity-columns" style="display:grid;grid-template-columns:1fr 1fr;gap:16px">
          <div class="activity-col">
            <h3 class="col-title" style="margin:0 0 8px;font-size:1rem;color:var(--muted);font-weight:700">Interactions</h3>
            <div class="activity-list" id="interactionActivityList">
              <div class="empty-state">
                <div style="font-size:42px;opacity:.6">ð¬</div>
                <p>No interactions yet</p>
              </div>
            </div>
          </div>
          <div class="activity-col">
            <h3 class="col-title" style="margin:0 0 8px;font-size:1rem;color:var(--muted);font-weight:700">Sales</h3>
            <div class="activity-list" id="salesActivityList">
              <div class="empty-state">
                <div style="font-size:42px;opacity:.6">ð°</div>
                <p>No sales yet</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Clients -->
    <div id="clients" class="tab-content" style="display:none">
      <div class="card">
        <div style="display:flex;justify-content:space-between;align-items:center;gap:10px;flex-wrap:wrap;margin-bottom:12px">
          <h2 style="margin:0">Client Management</h2>
          <button id="openClientBtn" class="btn primary">+ Add New Client</button>
        </div>

        <div class="search">
          <input type="text" id="clientSearch" placeholder="Search clients by name, email, phone, style...">
          <div class="row">
            <select id="clientSort">
              <option value="createdAt_desc">Sort: Recently Added</option>
              <option value="lastInteraction_desc">Sort: Last Interaction (NewestâOldest)</option>
              <option value="lastInteraction_asc">Sort: Last Interaction (OldestâNewest)</option>
              <option value="lastName_asc">Sort: Last Name (AâZ)</option>
              <option value="lastName_desc">Sort: Last Name (ZâA)</option>
              <option value="style_asc">Sort: Style (AâZ)</option>
              <option value="style_desc">Sort: Style (ZâA)</option>
              <option value="spent_desc">Sort: Amount Spent (HighâLow)</option>
              <option value="spent_asc">Sort: Amount Spent (LowâHigh)</option>
            </select>
          </div>
        </div>

        <!-- Style Filters (compact) -->
        <div class="filters">
          <div class="filters-row">
            <div class="filters-title">Filter by Style:</div>
            <label class="chk"><input type="checkbox" class="style-filter" value="Bohemian"> Bohemian</label>
            <label class="chk"><input type="checkbox" class="style-filter" value="Classic"> Classic</label>
            <label class="chk"><input type="checkbox" class="style-filter" value="Edgy"> Edgy</label>
            <label class="chk"><input type="checkbox" class="style-filter" value="Casual"> Casual</label>
            <label class="chk"><input type="checkbox" class="style-filter" value="Vintage"> Vintage</label>
            <label class="chk"><input type="checkbox" class="style-filter" value="Trendy"> Trendy</label>
          </div>
          <div class="filters-controls">
            <select id="styleMatch">
              <option value="any">Match any selected</option>
              <option value="all">Match all selected</option>
            </select>
            <button class="btn ghost" id="clearFiltersBtn" type="button">Clear Filters</button>
          </div>
        </div>

        <div class="list" id="clientList">
          <div class="empty-state">
            <div style="font-size:42px;opacity:.6">ð¥</div>
            <p>No clients yet. Add your first client!</p>
          </div>
        </div>
      </div>
    </div>

    <!-- Interactions -->
    <div id="interactions" class="tab-content" style="display:none">
      <div class="card">
        <div style="display:flex;justify-content:space-between;align-items:center;gap:10px;flex-wrap:wrap;margin-bottom:12px">
          <h2 style="margin:0">Interaction Tracking</h2>
          <button id="openInteractionBtn" class="btn primary">+ Log Interaction</button>
        </div>

        <div class="search">
          <input type="text" id="interactionSearch" placeholder="Search interactions...">
        </div>

        <div class="list" id="interactionList">
          <div class="empty-state">
            <div style="font-size:42px;opacity:.6">ð¬</div>
            <p>No interactions logged yet</p>
          </div>
        </div>
      </div>
    </div>

    <!-- Sales -->
    <div id="sales" class="tab-content" style="display:none">
      <div class="card">
        <div style="display:flex;justify-content:space-between;align-items:center;gap:10px;flex-wrap:wrap;margin-bottom:12px">
          <h2 style="margin:0">Sales Tracking</h2>
          <button id="openSaleBtn" class="btn primary">+ Record Sale</button>
        </div>

        <div class="list" id="salesList">
          <div class="empty-state">
            <div style="font-size:42px;opacity:.6">ð°</div>
            <p>No sales data available</p>
          </div>
        </div>
      </div>
    </div>

    <!-- Follow Up -->
    <div id="followups" class="tab-content" style="display:none">
      <div class="card">
        <div style="display:flex;justify-content:space-between;align-items:center;gap:10px;flex-wrap:wrap;margin-bottom:12px">
          <h2 style="margin:0">Follow Up</h2>
          <button id="openFollowUpBtn" class="btn primary">+ Add Follow Up</button>
        </div>
        <div class="followup-sections">
          <div>
            <h3>Past Due</h3>
            <div id="followupPastDue" class="list"></div>
          </div>
          <div>
            <h3>Upcoming</h3>
            <div id="followupUpcoming" class="list"></div>
          </div>
          <div>
            <h3>Future</h3>
            <div id="followupFuture" class="list"></div>
          </div>
          <div>
            <h3>ð¨ 911</h3>
            <div id="followup911" class="list"></div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- Client Modal -->
  <div id="clientModal" class="modal">
    <div class="panel">
      <header>
        <h3 id="clientModalTitle" style="margin:0">Add New Client</h3>
        <button class="x" data-close-modal>Ã</button>
      </header>
      <form id="clientForm" onsubmit="saveClient(event)">
        <div class="row-cols">
          <div><label>First Name *</label><input type="text" id="clientFirstName" required></div>
          <div><label>Last Name *</label><input type="text" id="clientLastName" required></div>
        </div>
        <div class="row-cols">
          <div><label>Email</label><input type="email" id="clientEmail"></div>
          <div><label>Phone</label><input type="tel" id="clientPhone"></div>
        </div>
        <div>
          <label>Style Vibe (choose one or more)</label>
          <select id="clientStyles" multiple size="6">
            <option>Bohemian</option><option>Classic</option><option>Edgy</option>
            <option>Casual</option><option>Vintage</option><option>Trendy</option>
          </select>
        </div>
        <div class="row-cols">
          <div>
            <label>Status</label>
            <select id="clientStatus">
              <option>Introductory</option>
              <option>First Appointment</option>
              <option>Established</option>
            </select>
          </div>
          <div>
            <label>Initial Sales Amount</label>
            <input type="number" id="clientInitialSales" min="0" step="0.01" placeholder="0.00">
          </div>
        </div>
        <div>
          <label>Notes</label>
          <textarea id="clientNotes" placeholder="Add any notes about this client..."></textarea>
        </div>
        <div style="display:flex;gap:10px;justify-content:flex-end;margin-top:8px">
          <button type="button" class="btn ghost" data-close-modal>Cancel</button>
          <button type="submit" class="btn primary">Save Client</button>
        </div>
      </form>
    </div>
  </div>

  <!-- Client Recap Modal -->
  <div id="clientViewModal" class="modal">
    <div class="panel" id="clientViewPanel">
      <header>
        <h3 style="margin:0">Client Recap</h3>
        <button class="x" data-close-modal>Ã</button>
      </header>
      <div id="clientViewBody"></div>
      <div style="display:flex;justify-content:flex-end;margin-top:12px">
        <button class="btn primary" data-close-modal>Close</button>
      </div>
    </div>
  </div>

  <!-- Interaction Modal -->
  <div id="interactionModal" class="modal">
    <div class="panel">
      <header>
        <h3 id="interactionModalTitle" style="margin:0">Log Interaction</h3>
        <button class="x" data-close-modal>Ã</button>
      </header>
      <form id="interactionForm" onsubmit="saveInteraction(event)">
        <div>
          <label>Client *</label>
          <select id="interactionClient" required><option value="">Select client...</option></select>
        </div>
        <div class="row-cols">
          <div>
            <label>Type *</label>
            <select id="interactionType" required>
              <option>Call</option>
              <option>Email</option>
              <option>Text</option>
              <option>In-person</option>
            </select>
          </div>
          <div>
            <label>Date *</label>
            <input type="date" id="interactionDate" required>
          </div>
        </div>
        <div><label>Notes</label><textarea id="interactionNotes" placeholder="Describe the interaction..."></textarea></div>
        <div class="card-actions" style="justify-content:flex-end">
          <button type="button" class="btn ghost" data-close-modal>Cancel</button>
          <button type="submit" class="btn primary">Save Interaction</button>
        </div>
      </form>
    </div>
  </div>

  <!-- Sale Modal -->
  <div id="saleModal" class="modal">
    <div class="panel">
      <header>
        <h3 id="saleModalTitle" style="margin:0">Record Sale</h3>
        <button class="x" data-close-modal>Ã</button>
      </header>
      <form id="saleForm" onsubmit="saveSale(event)">
        <div>
          <label>Client *</label>
          <select id="saleClient" required><option value="">Select client...</option></select>
        </div>
        <div class="row-cols">
          <div><label>Amount *</label><input type="number" id="saleAmount" min="0" step="0.01" required placeholder="0.00"></div>
          <div><label>Date *</label><input type="date" id="saleDate" required></div>
        </div>
        <div><label>Description</label><input type="text" id="saleDescription" placeholder="What was sold?"></div>
        <div class="card-actions" style="justify-content:flex-end">
          <button type="button" class="btn ghost" data-close-modal>Cancel</button>
          <button type="submit" class="btn primary">Save Sale</button>
        </div>
      </form>
    </div>
  </div>

  <!-- Follow Up Modal -->
  <div id="followupModal" class="modal">
    <div class="panel">
      <header>
        <h3 style="margin:0">Add Follow Up</h3>
        <button class="x" data-close-modal>Ã</button>
      </header>
      <form id="followupForm" onsubmit="saveFollowUp(event)">
        <div>
          <label>Client *</label>
          <select id="followupClient" required><option value="">Select client...</option></select>
        </div>
        <div class="row-cols">
          <div><label>Due Date *</label><input type="date" id="followupDate" required></div>
        </div>
        <div><label>Notes</label><textarea id="followupNotes" placeholder="Follow up details..."></textarea></div>
        <div class="card-actions" style="justify-content:flex-end">
          <button type="button" class="btn ghost" data-close-modal>Cancel</button>
          <button type="submit" class="btn primary">Save Follow Up</button>
        </div>
      </form>
    </div>
  </div>

<script>
  // ---------- Utilities ----------
  const fmtUSD = new Intl.NumberFormat('en-US', { style: 'currency', currency: 'USD', maximumFractionDigits: 2 });
  const $  = (s, r=document) => r.querySelector(s);
  const $$ = (s, r=document) => [...r.querySelectorAll(s)];
  const escapeHTML = (str) => String(str ?? '')
  .replace(/&/g, '&amp;')
  .replace(/</g, '&lt;')
  .replace(/>/g, '&gt;')
  .replace(/"/g, '&quot;')
  .replace(/'/g, '&#039;');

  // Status helpers
  const VALID_STATUSES = ["Introductory","First Appointment","Established"];
  const statusSlug = s => String(s||"").toLowerCase().replace(/\s+/g,'-');
  const mapOldStatus = s => ({ "Prospect":"Introductory","Active":"Established","Inactive":"Introductory" }[s] || (VALID_STATUSES.includes(s)? s : "Introductory"));

  // Styles config + helpers
  const ALLOWED_STYLES = ["Bohemian","Classic","Edgy","Casual","Vintage","Trendy"];
  const getSelectedValues = (selectEl) => [...selectEl.options].filter(o => o.selected).map(o => o.value);
  const normalizeStyles = (arrOrStr) => {
    if (Array.isArray(arrOrStr)) return arrOrStr.filter(v => ALLOWED_STYLES.includes(v));
    if (typeof arrOrStr === 'string' && arrOrStr.trim()) {
      const parts = arrOrStr.split(',').map(s => s.trim()).filter(Boolean);
      return parts.filter(v => ALLOWED_STYLES.includes(v));
    }
    return [];
  };

  // ---------- Data ----------
  let clients = [];        // {id, firstName, lastName, email, phone, styles[], status, initialSales, notes, createdAt}
  let interactions = [];   // {id, clientId, type, date(YYYY-MM-DD), notes, createdAt}
  let sales = [];          // {id, clientId, amount, date(YYYY-MM-DD), description, createdAt, interactionId?}
  let followUps = [];      // {id, clientId, date(YYYY-MM-DD), notes, createdAt, completed, completedAt, type}
  let editingClientId = null;
  let editingInteractionId = null;
  let editingSaleId = null;

  // ---------- Local Storage + Backup ----------
  function saveData() {
    localStorage.setItem('crm_clients', JSON.stringify(clients));
    localStorage.setItem('crm_interactions', JSON.stringify(interactions));
    localStorage.setItem('crm_sales', JSON.stringify(sales));
    localStorage.setItem('crm_followups', JSON.stringify(followUps));
  }
  function loadData() {
    try {
      clients = JSON.parse(localStorage.getItem('crm_clients') || '[]');
      interactions = JSON.parse(localStorage.getItem('crm_interactions') || '[]');
      sales = JSON.parse(localStorage.getItem('crm_sales') || '[]');
      followUps = JSON.parse(localStorage.getItem('crm_followups') || '[]');

      // Migration tweaks
      let migrated = false;
      clients.forEach(c => {
        if (!c.firstName && c.name) {
          const parts = String(c.name).trim().split(/\s+/);
          c.firstName = parts.shift() || '';
          c.lastName = parts.join(' ');
          delete c.name; migrated = true;
        }
        if (!c.styles) { c.styles = normalizeStyles(c.style); delete c.style; migrated = true; }
        else { c.styles = normalizeStyles(c.styles); }
        const mapped = mapOldStatus(c.status);
        if (mapped !== c.status) { c.status = mapped; migrated = true; }
      });
      interactions.forEach(i => { if (i.date && i.date.length > 10) { i.date = i.date.slice(0,10); migrated = true; } });
      followUps.forEach(f => { if (f.completed === undefined) { f.completed = false; f.type = 'manual'; migrated = true; } });
      if (migrated) saveData();
    } catch(e) {
      console.warn('Failed to load saved data:', e);
      clients = []; interactions = []; sales = []; followUps = [];
    }
  }

  function exportData() {
    const payload = { exportedAt: new Date().toISOString(), version: 1, clients, interactions, sales, followUps };
    const blob = new Blob([JSON.stringify(payload, null, 2)], { type: 'application/json' });
    const url = URL.createObjectURL(blob);
    const a = document.createElement('a');
    a.href = url; a.download = 'crm-backup.json';
    document.body.appendChild(a); a.click(); a.remove(); URL.revokeObjectURL(url);
  }
  function importData(file) {
    const reader = new FileReader();
    reader.onload = () => {
      try {
        const data = JSON.parse(reader.result);
        if (!data || !Array.isArray(data.clients) || !Array.isArray(data.interactions) || !Array.isArray(data.sales)) {
          alert('Invalid file format.'); return;
        }
        clients = data.clients.map(c => ({
          ...c,
          styles: normalizeStyles(c.styles ?? c.style),
          status: mapOldStatus(c.status),
          initialSales: Number(c.initialSales) || 0
        }));
        interactions = data.interactions.map(i => ({ ...i, date: (i.date||'').slice(0,10) }));
        sales = data.sales.map(s => ({ ...s, amount: Number(s.amount) || 0 }));
        followUps = (data.followUps || []).map(f => ({ ...f, date: (f.date||'').slice(0,10) }));
        saveData(); renderClients(); renderInteractions(); renderSalesView(); renderFollowUps(); updateDashboard();
        alert('Import complete âï¸');
      } catch (e) { console.error(e); alert('Could not parse the file.'); }
    };
    reader.readAsText(file);
  }

  // ---------- Startup ----------
  document.addEventListener('DOMContentLoaded', () => {
    loadData();
    renderClients(); renderInteractions(); renderSalesView(); renderFollowUps(); updateDashboard();

    // Default dates
    const today = new Date().toISOString().slice(0,10);
    ['interactionDate','saleDate','followupDate'].forEach(id => { const el = document.getElementById(id); if (el) el.value = today; });

    // ESC to close modals
    document.addEventListener('keydown', e => { if (e.key === 'Escape') closeAllModals(); });

    // Click outside panel closes modal
    document.addEventListener('click', e => {
      const m = e.target.closest('.modal');
      if (m && !e.target.closest('.panel')) m.classList.remove('active');
    });

    // Filters & search wiring
    $$('.style-filter').forEach(cb => cb.addEventListener('change', applyFiltersAndSort));
    const styleMatchSel = $('#styleMatch'); if (styleMatchSel) styleMatchSel.addEventListener('change', applyFiltersAndSort);
    $('#clearFiltersBtn')?.addEventListener('click', () => {
      $$('.style-filter').forEach(cb => cb.checked = false);
      if (styleMatchSel) styleMatchSel.value = 'any';
      applyFiltersAndSort();
    });
    $('#clientSearch')?.addEventListener('input', applyFiltersAndSort);
    $('#clientSort')?.addEventListener('change', applyFiltersAndSort);
    $('#interactionSearch')?.addEventListener('input', searchInteractions);

    // Header buttons
    $('#exportBtn')?.addEventListener('click', exportData);
    const importBtn = $('#importBtn'), importFile = $('#importFile');
    if (importBtn && importFile) {
      importBtn.addEventListener('click', () => importFile.click());
      importFile.addEventListener('change', (e) => {
        const file = e.target.files[0];
        if (file) importData(file);
        importFile.value = '';
      });
    }
    $('#clearBtn')?.addEventListener('click', () => {
      if (confirm('Clear ALL clients, interactions, sales, and follow ups? This cannot be undone.')) {
        clients = []; interactions = []; sales = []; followUps = [];
        saveData(); renderClients(); renderInteractions(); renderSalesView(); renderFollowUps(); updateDashboard();
      }
    });

    // Tabs
    const tabs = $$('.tab');
    tabs.forEach(btn => btn.addEventListener('click', () => switchTab(btn.dataset.tab)));
    const tabList = $('.tabs[role="tablist"]');
    tabList?.addEventListener('keydown', (e) => {
      const keys = ['ArrowLeft','ArrowRight','Home','End'];
      if (!keys.includes(e.key)) return;
      e.preventDefault();
      const i = tabs.indexOf(document.activeElement);
      if (i === -1) return;
      let t = i;
      if (e.key === 'ArrowLeft') t = (i - 1 + tabs.length) % tabs.length;
      if (e.key === 'ArrowRight') t = (i + 1) % tabs.length;
      if (e.key === 'Home') t = 0;
      if (e.key === 'End') t = tabs.length - 1;
      tabs[t].focus(); switchTab(tabs[t].dataset.tab);
    });

    // Modal openers
    $('#openClientBtn')?.addEventListener('click', () => openClientModal());
    $('#openInteractionBtn')?.addEventListener('click', () => { try { openInteractionModal(); } catch (e){ alert('Could not open the interaction window.'); }});
    $('#openSaleBtn')?.addEventListener('click', () => openSaleModal());
    $('#openFollowUpBtn')?.addEventListener('click', () => openFollowUpModal());

    // Any [data-close-modal]
    document.addEventListener('click', (e) => {
      const btn = e.target.closest('[data-close-modal]');
      if (!btn) return;
      const modal = btn.closest('.modal');
      if (!modal) return;
      modal.classList.remove('active');
      modal.querySelector('form')?.reset();
      if (modal.id === 'interactionModal') editingInteractionId = null;
      if (modal.id === 'saleModal') editingSaleId = null;
    });

    // Delegated actions for client list
    $('#clientList')?.addEventListener('click', (e) => {
      const btn = e.target.closest('button[data-action]');
      if (!btn) return;
      const id = btn.getAttribute('data-id');
      const action = btn.getAttribute('data-action');
      if (!id || !action) return;
      if (action === 'view') openClientView(id);
      if (action === 'edit') openClientModal(id);
      if (action === 'delete') deleteClient(id);
    });

    // Delegated delete/edit for interactions
    $('#interactionList')?.addEventListener('click', (e) => {
      const delBtn = e.target.closest('button[data-action="delete-interaction"]');
      if (delBtn) { const id = delBtn.getAttribute('data-id'); if (id) deleteInteraction(id); return; }
      const editBtn = e.target.closest('button[data-action="edit-interaction"]');
      if (editBtn) { const id = editBtn.getAttribute('data-id'); if (id) openInteractionModal(id); return; }
    });

    // Delegated toggle/delete for follow-ups (and 911 "create" action)
    document.addEventListener('click', (e) => {
      const toggleBtn = e.target.closest('button[data-action="toggle-followup"]');
      if (toggleBtn) { const id = toggleBtn.getAttribute('data-id'); if (id) toggleFollowUp(id); return; }
      const deleteBtn = e.target.closest('button[data-action="delete-followup"]');
      if (deleteBtn) { const id = deleteBtn.getAttribute('data-id'); if (id) deleteFollowUp(id); return; }
      const createBtn = e.target.closest('button[data-action="create-followup-for-client"]');
      if (createBtn) {
        const id = createBtn.getAttribute('data-id');
        const notes = createBtn.getAttribute('data-notes') || '';
        if (id) openFollowUpModal(id, notes);
        return;
      }
    });

    // Delegated edit/delete for sales
    $('#salesList')?.addEventListener('click', (e) => {
      const editBtn = e.target.closest('button[data-action="edit-sale"]');
      if (editBtn) { const id = editBtn.getAttribute('data-id'); if (id) openSaleModal(id); return; }
      const delBtn = e.target.closest('button[data-action="delete-sale"]');
      if (delBtn) { const id = delBtn.getAttribute('data-id'); if (id) deleteSale(id); return; }
    });
  });

  function closeAllModals(){ $$('.modal.active').forEach(m => m.classList.remove('active')); }

  // ---------- Tabs ----------
  function switchTab(tabName){
    $$('.tab-content').forEach(c => {
      const active = c.id === tabName;
      c.style.display = active ? 'block' : 'none';
      if (active) { c.setAttribute('role','region'); c.setAttribute('aria-label', tabName); }
    });
    $$('.tab').forEach(b => {
      const active = b.dataset.tab === tabName;
      b.classList.toggle('active', active);
      b.setAttribute('aria-selected', active ? 'true' : 'false');
      b.tabIndex = active ? 0 : -1;
    });
    if (tabName === 'dashboard') updateDashboard();
    if (tabName === 'sales') renderSalesView();
    if (tabName === 'followups') renderFollowUps();
  }

  // ---------- Helpers ----------
  const fullNameOf = (c) => `${c.firstName ?? ''} ${c.lastName ?? ''}`.trim();
  const lastNameKey = (c) => (c.lastName || '').toLowerCase();
  function getActiveStyleFilters(){ return Array.from(document.querySelectorAll('.style-filter:checked')).map(c => c.value); }
  function lastInteractionDate(clientId){
    const ds = interactions.filter(i => i.clientId === clientId).map(i => new Date(i.date));
    return ds.length ? new Date(Math.max(...ds)) : null;
  }

  // ---------- Auto Follow-up Creation ----------
  function createAutoFollowUp(clientId, baseDate, type) {
    const date = new Date(baseDate);
    let notes;
    if (type === 'weekly') { date.setDate(date.getDate() + 7); notes = 'Weekly follow-up (auto-created)'; }
    else if (type === 'monthly') { date.setMonth(date.getMonth() + 1); notes = 'Monthly follow-up (auto-created)'; }
    followUps.push({
      id: Date.now().toString() + Math.random().toString(36).substr(2, 5),
      clientId, date: date.toISOString().slice(0, 10), notes,
      createdAt: new Date().toISOString(), completed: false, type
    });
  }

  function toggleFollowUp(id) {
    const f = followUps.find(x => x.id === id);
    if (!f) return;
    f.completed = !f.completed;
    f.completedAt = f.completed ? new Date().toISOString() : null;
    if (f.completed && f.type === 'weekly') createAutoFollowUp(f.clientId, f.completedAt.slice(0,10), 'monthly');
    saveData(); renderFollowUps(); updateDashboard();
  }

  function deleteFollowUp(id) {
    const f = followUps.find(x => x.id === id);
    if (!f) return;
    const isAuto = f.type !== 'manual';
    const ok = confirm(isAuto ? 'Delete this auto-created follow-up?' : 'Delete this follow-up?');
    if (!ok) return;
    followUps = followUps.filter(x => x.id !== id);
    saveData(); renderFollowUps(); updateDashboard();
  }

  // ---------- Clients ----------
  function openClientModal(clientId=null){
    editingClientId = clientId;
    const modal = $('#clientModal');
    const form = $('#clientForm');

    if (clientId){
      const c = clients.find(x => x.id === clientId);
      $('#clientModalTitle').textContent = 'Edit Client';
      $('#clientFirstName').value = c.firstName || '';
      $('#clientLastName').value  = c.lastName || '';
      $('#clientEmail').value     = c.email || '';
      $('#clientPhone').value     = c.phone || '';
      const sel = $('#clientStyles');
      const arr = normalizeStyles(c.styles ?? c.style);
      [...sel.options].forEach(o => o.selected = arr.includes(o.value));
      $('#clientStatus').value    = VALID_STATUSES.includes(c.status)? c.status : 'Introductory';
      $('#clientInitialSales').value = c.initialSales ?? '';
      $('#clientNotes').value     = c.notes || '';
    } else {
      $('#clientModalTitle').textContent = 'Add New Client';
      form.reset();
      $('#clientStatus').value = 'Introductory';
      [...$('#clientStyles').options].forEach(o => o.selected = false);
    }

    modal.classList.add('active');
    setTimeout(()=>{ modal.querySelector('input,select,textarea,button')?.focus(); },0);
  }
  function closeClientModal(){ $('#clientModal').classList.remove('active'); $('#clientForm').reset(); editingClientId=null; }

  function saveClient(e){
    e.preventDefault();
    const firstName = $('#clientFirstName').value.trim();
    const lastName  = $('#clientLastName').value.trim();
    if (!firstName || !lastName){ alert('First and last names are required.'); return; }

    const clientData = {
      firstName, lastName,
      email: $('#clientEmail').value.trim(),
      phone: $('#clientPhone').value.trim(),
      styles: normalizeStyles(getSelectedValues($('#clientStyles'))),
      status: $('#clientStatus').value || 'Introductory',
      initialSales: parseFloat($('#clientInitialSales').value) || 0,
      notes: $('#clientNotes').value.trim(),
      createdAt: new Date().toISOString()
    };

    if (editingClientId){
      const i = clients.findIndex(c => c.id === editingClientId);
      clients[i] = { ...clients[i], ...clientData };
    } else {
      clientData.id = Date.now().toString();
      clients.push(clientData);
    }
    saveData(); closeClientModal(); renderClients(); renderFollowUps(); updateDashboard();
  }

  function deleteClient(clientId){
    if (!confirm('Delete this client and all related interactions, sales, and follow ups?')) return;
    clients = clients.filter(c => c.id !== clientId);
    interactions = interactions.filter(i => i.clientId !== clientId);
    sales = sales.filter(s => s.clientId !== clientId);
    followUps = followUps.filter(f => f.clientId !== clientId);
    saveData(); renderClients(); renderFollowUps(); updateDashboard();
  }

  function totalSpentFor(clientId){
    const c = clients.find(x => x.id === clientId);
    const extra = sales.filter(s => s.clientId === clientId).reduce((sum, s) => sum + (Number(s.amount) || 0), 0);
    return (Number(c?.initialSales) || 0) + extra;
  }

  function renderClients(source = clients){
    const list = $('#clientList');
    if (source.length === 0){
      list.innerHTML = `
        <div class="empty-state">
          <div style="font-size:42px;opacity:.6">ð¥</div>
          <p>No clients yet. Add your first client!</p>
        </div>`;
      return;
    }

    const sorted = sortClients([...source], $('#clientSort').value || 'createdAt_desc');

    list.innerHTML = sorted.map(c => {
      const totalSpent = totalSpentFor(c.id);
      const li = lastInteractionDate(c.id);
      return `
        <div class="client-item" data-client-id="${c.id}">
          <div class="client-header">
            <div>
              <div class="client-name">
                ${escapeHTML(fullNameOf(c))}
                ${totalSpent > 0 ? `<span class="badge-sale">${fmtUSD.format(totalSpent)}</span>` : ''}
              </div>
              <div class="muted" style="margin-top:4px">
                ${c.email ? `ð§ ${escapeHTML(c.email)} Â· ` : ''}${c.phone ? `ð± ${escapeHTML(c.phone)}` : ''}
              </div>
              ${(c.styles && c.styles.length) ? `
                <div class="tags" aria-label="Style Vibes">
                  ${c.styles.map(s => `<span class="tag">${escapeHTML(s)}</span>`).join('')}
                </div>` : ''}
              ${li ? `<div class="muted" style="margin-top:6px;font-size:.85rem">Last Interaction: ${li.toLocaleDateString()}</div>` : ''}
            </div>
            <span class="chip status-${statusSlug(c.status||'Introductory')}">
              ${escapeHTML(c.status || 'Introductory')}
            </span>
          </div>
          <div class="buttons">
            <button class="btn primary" data-action="view"  data-id="${c.id}">View</button>
            <button class="btn ghost"   data-action="edit"  data-id="${c.id}">Edit</button>
            <button class="btn danger"  data-action="delete" data-id="${c.id}">Delete</button>
          </div>
        </div>`;
    }).join('');
  }

  function searchClients(){ applyFiltersAndSort(); }
  function applyClientSort(){ applyFiltersAndSort(); }

  function sortClients(arr, mode){
    const bySpent = (a,b) => totalSpentFor(a.id) - totalSpentFor(b.id);
    const byLast  = (a,b) => lastNameKey(a).localeCompare(lastNameKey(b));
    const byStyle = (a,b) => {
      const sa = (a.styles && a.styles.length) ? [...a.styles].sort()[0] : '';
      const sb = (b.styles && b.styles.length) ? [...b.styles].sort()[0] : '';
      return sa.toLowerCase().localeCompare(sb.toLowerCase());
    };
    const byCreatedDesc = (a,b) => new Date(b.createdAt) - new Date(a.createdAt);

    switch(mode){
      case 'lastInteraction_desc':
        return arr.sort((a,b)=>{
          const da = lastInteractionDate(a.id), db = lastInteractionDate(b.id);
          if (da && db) return db - da;
          if (da && !db) return -1;
          if (!da && db) return 1;
          return byLast(a,b);
        });
      case 'lastInteraction_asc':
        return arr.sort((a,b)=>{
          const da = lastInteractionDate(a.id), db = lastInteractionDate(b.id);
          if (da && db) return da - db;
          if (da && !db) return -1;
          if (!da && db) return 1;
          return byLast(a,b);
        });
      case 'lastName_asc':  return arr.sort((a,b) => byLast(a,b));
      case 'lastName_desc': return arr.sort((a,b) => byLast(b,a));
      case 'style_asc':     return arr.sort((a,b) => byStyle(a,b) || byLast(a,b));
      case 'style_desc':    return arr.sort((a,b) => byStyle(b,a) || byLast(a,b));
      case 'spent_asc':     return arr.sort((a,b) => bySpent(a,b) || byLast(a,b));
      case 'spent_desc':    return arr.sort((a,b) => bySpent(b,a) || byLast(a,b));
      case 'createdAt_desc':
      default:              return arr.sort(byCreatedDesc);
    }
  }

  function applyFiltersAndSort(){
    const term = ($('#clientSearch').value || '').toLowerCase();
    const selected = getActiveStyleFilters();
    const matchModeEl = $('#styleMatch');
    const matchMode = matchModeEl ? matchModeEl.value : 'any';

    let list = clients.filter(c => {
      const matchesSearch =
        fullNameOf(c).toLowerCase().includes(term) ||
        (c.email && c.email.toLowerCase().includes(term)) ||
        (c.phone && c.phone.includes(term)) ||
        (c.styles && c.styles.some(s => s.toLowerCase().includes(term)));

      if (!matchesSearch) return false;

      if (!selected.length) return true;
      const styles = c.styles || [];
      return (matchMode === 'all')
        ? selected.every(s => styles.includes(s))
        : selected.some(s => styles.includes(s));
    });

    const mode = $('#clientSort').value || 'createdAt_desc';
    list = sortClients(list, mode);
    renderClients(list);
  }

  // ---------- Client View ----------
  function openClientView(clientId){
    const c = clients.find(x => x.id === clientId);
    if (!c) return;
    const total = totalSpentFor(clientId);
    const its   = interactions.filter(i => i.clientId === clientId).sort((a,b) => new Date(b.date)-new Date(a.date));
    const lastIt = its[0];
    const clSales = sales.filter(s => s.clientId === clientId).sort((a,b) => new Date(b.date)-new Date(a.date));

    $('#clientViewBody').innerHTML = `
      <div class="card" style="box-shadow:none;padding:0">
        <div style="display:flex;justify-content:space-between;gap:12px;align-items:flex-start">
          <div style="min-width:0">
            <h3 style="margin:0 0 6px">${escapeHTML(fullNameOf(c))}</h3>
            <div class="muted">
              ${c.email ? `ð§ ${escapeHTML(c.email)} Â· ` : ''}${c.phone ? `ð± ${escapeHTML(c.phone)}` : ''}
            </div>
            ${(c.styles && c.styles.length) ? `
              <div class="tags" style="margin-top:6px">
                ${c.styles.map(s => `<span class="tag">${escapeHTML(s)}</span>`).join('')}
              </div>` : ''}
            <span class="chip status-${statusSlug(c.status||'Introductory')}" style="margin-top:8px;display:inline-block">
              ${escapeHTML(c.status||'Introductory')}
            </span>
          </div>
          <div class="badge-sale">${fmtUSD.format(total)}</div>
        </div>

        ${c.notes ? `<div style="margin-top:12px"><strong>Notes:</strong><br>${escapeHTML(c.notes)}</div>` : ''}

        <div style="margin-top:16px;display:grid;gap:10px">
          <div><strong>Interactions:</strong> ${its.length}${lastIt ? ` â Last: ${new Date(lastIt.date).toLocaleDateString()}` : ''}</div>
          <div><strong>Initial Sales:</strong> ${fmtUSD.format(Number(c.initialSales) || 0)}</div>
        </div>

        <div style="margin-top:16px">
          <strong>Recent Sales</strong>
          ${clSales.length === 0 ? `<div class="muted">No sales recorded</div>` : `
            <div style="margin-top:8px;display:grid;gap:8px">
              ${clSales.slice(0,5).map(s => `
                <div style="display:flex;justify-content:space-between;border-bottom:1px solid #eee;padding-bottom:6px">
                  <div>
                    <div style="font-weight:600">${escapeHTML(s.description || 'Sale')}</div>
                    <div class="muted" style="font-size:.85rem">${new Date(s.date).toLocaleDateString()}</div>
                  </div>
                  <div style="font-weight:800;color:#2f855a">${fmtUSD.format(Number(s.amount) || 0)}</div>
                </div>`).join('')}
            </div>`}
        </div>
      </div>
    `;
    $('#clientViewModal').classList.add('active');
  }

  // ---------- Interactions ----------
  function openInteractionModal(interactionId=null){
    editingInteractionId = interactionId;
    const select = $('#interactionClient');
    const dateEl = $('#interactionDate');
    const modal  = $('#interactionModal');

    if (!select || !dateEl || !modal) { alert('Interaction form is missing.'); return; }

    // Populate clients
    select.innerHTML = '<option value="">Select client...</option>' +
      (clients||[]).map(c => `<option value="${c.id}">${escapeHTML(fullNameOf(c))}</option>`).join('');

    if (interactionId){
      const it = interactions.find(i => i.id === interactionId);
      if (!it) return;
      $('#interactionModalTitle').textContent = 'Edit Interaction';
      select.value = it.clientId;
      $('#interactionType').value = ['Call','Email','Text','In-person'].includes(it.type) ? it.type : 'Call';
      dateEl.value = it.date;
      $('#interactionNotes').value = it.notes || '';
    } else {
      $('#interactionModalTitle').textContent = 'Log Interaction';
      $('#interactionForm').reset();
      dateEl.value = new Date().toISOString().slice(0,10);
    }

    modal.classList.add('active');
    setTimeout(() => { modal.querySelector('input,select,textarea,button')?.focus(); }, 0);
  }
  function closeInteractionModal(){ $('#interactionModal').classList.remove('active'); $('#interactionForm').reset(); editingInteractionId=null; }

  function saveInteraction(e){
    e.preventDefault();
    const clientId = $('#interactionClient').value;
    if (!clientId){ alert('Please select a client'); return; }
    const interactionDate = $('#interactionDate').value || new Date().toISOString().slice(0,10);

    if (editingInteractionId){
      const idx = interactions.findIndex(i => i.id === editingInteractionId);
      if (idx !== -1){
        interactions[idx] = {
          ...interactions[idx],
          clientId,
          type: $('#interactionType').value,
          date: interactionDate,
          notes: $('#interactionNotes').value.trim()
        };
      }
    } else {
      const newId = Date.now().toString();
      interactions.push({
        id: newId, clientId,
        type: $('#interactionType').value,
        date: interactionDate,
        notes: $('#interactionNotes').value.trim(),
        createdAt: new Date().toISOString()
      });
      // Auto follow-up
      createAutoFollowUp(clientId, interactionDate, 'weekly');
    }

    saveData(); closeInteractionModal(); renderInteractions(); renderFollowUps(); updateDashboard();
  }

  function renderInteractions(source = interactions){
    const el = $('#interactionList');
    if (source.length === 0){
      el.innerHTML = `
        <div class="empty-state">
          <div style="font-size:42px;opacity:.6">ð¬</div>
          <p>No interactions logged yet</p>
        </div>`;
      return;
    }
    const sorted = [...source].sort((a,b) => new Date(b.date) - new Date(a.date));
    el.innerHTML = sorted.map(i => {
      const c = clients.find(x => x.id === i.clientId);
      const when = new Date(i.date).toLocaleDateString([], { year:'numeric', month:'short', day:'numeric' });
      const isSale = i.type === 'Sale';
      return `
        <div class="interaction-item">
          <div class="client-header">
            <div>
              <div class="client-name">${escapeHTML(c ? fullNameOf(c) : 'Unknown Client')}</div>
              <div class="muted" style="margin-top:4px">${escapeHTML(i.type)} â¢ ${when}</div>
            </div>
            <div class="buttons">
              ${isSale ? '' : `<button class="btn ghost"  data-action="edit-interaction" data-id="${i.id}">Edit</button>`}
              <button class="btn danger" data-action="delete-interaction" data-id="${i.id}">Delete</button>
            </div>
          </div>
          ${i.notes ? `<div class="notes" style="margin-top:8px">${escapeHTML(i.notes)}</div>` : ''}
        </div>`;
    }).join('');
  }

  function deleteInteraction(id){
    if (!confirm('Delete this interaction?')) return;
    // If this interaction is linked to a sale, clear the link
    const saleIdx = sales.findIndex(s => s.interactionId === id);
    if (saleIdx !== -1) sales[saleIdx].interactionId = undefined;
    interactions = interactions.filter(i => i.id !== id);
    saveData(); renderInteractions(); updateDashboard(); renderFollowUps();
  }

  function searchInteractions(){
    const term = ($('#interactionSearch').value||'').toLowerCase();
    const filtered = interactions.filter(i => {
      const c = clients.find(x => x.id === i.clientId);
      return (c && fullNameOf(c).toLowerCase().includes(term)) ||
             i.type.toLowerCase().includes(term) ||
             (i.notes && i.notes.toLowerCase().includes(term));
    });
    renderInteractions(filtered);
  }

  // ---------- Sales ----------
  function openSaleModal(saleId=null){
    editingSaleId = saleId;
    const select = $('#saleClient');
    const modal = $('#saleModal');

    // populate clients
    select.innerHTML = '<option value="">Select client...</option>' +
      clients.map(c => `<option value="${c.id}">${escapeHTML(fullNameOf(c))}</option>`).join('');

    if (saleId){
      const s = sales.find(x => x.id === saleId);
      if (!s) return;
      $('#saleModalTitle').textContent = 'Edit Sale';
      select.value = s.clientId;
      $('#saleAmount').value = s.amount;
      $('#saleDate').value = s.date;
      $('#saleDescription').value = s.description || '';
    } else {
      $('#saleModalTitle').textContent = 'Record Sale';
      $('#saleForm').reset();
      $('#saleDate').value = new Date().toISOString().slice(0,10);
    }

    modal.classList.add('active');
    setTimeout(() => { modal.querySelector('input,select,textarea,button')?.focus(); }, 0);
  }
  function closeSaleModal(){ $('#saleModal').classList.remove('active'); $('#saleForm').reset(); editingSaleId=null; }

  function saveSale(e){
    e.preventDefault();
    const clientId = $('#saleClient').value;
    const amount = parseFloat($('#saleAmount').value);
    const date = $('#saleDate').value || new Date().toISOString().slice(0,10);
    const description = $('#saleDescription').value.trim();

    if (!clientId || isNaN(amount)){ alert('Client and amount are required'); return; }

    if (editingSaleId){
      const idx = sales.findIndex(s => s.id === editingSaleId);
      if (idx !== -1){
        // Update sale
        sales[idx] = { ...sales[idx], clientId, amount, date, description };

        // Update paired interaction if present
        const iId = sales[idx].interactionId;
        if (iId){
          const iIdx = interactions.findIndex(i => i.id === iId);
          if (iIdx !== -1){
            interactions[iIdx] = {
              ...interactions[iIdx],
              clientId,
              date,
              type: 'Sale',
              notes: `Sale recorded: ${fmtUSD.format(amount)}${description ? ` â ${description}` : ''}`
            };
          }
        }
      }
    } else {
      // Create sale
      const id = Date.now().toString();
      const sale = { id, clientId, amount, date, description, createdAt: new Date().toISOString() };
      sales.push(sale);

      // Create paired interaction
      const interactionId = 'sale-' + id;
      interactions.push({
        id: interactionId,
        clientId,
        type: 'Sale',
        date,
        notes: `Sale recorded: ${fmtUSD.format(amount)}${description ? ` â ${description}` : ''}`,
        createdAt: new Date().toISOString()
      });
      // store link
      const sIdx = sales.findIndex(s => s.id === id);
      if (sIdx !== -1) sales[sIdx].interactionId = interactionId;
    }

    saveData(); closeSaleModal(); renderSalesView(); renderInteractions(); renderFollowUps(); updateDashboard(); renderClients();
  }

  function deleteSale(id){
    if (!confirm('Delete this sale?')) return;
    const s = sales.find(x => x.id === id);
    if (s && s.interactionId){
      // also delete paired interaction
      interactions = interactions.filter(i => i.id !== s.interactionId);
    }
    sales = sales.filter(s => s.id !== id);
    saveData(); renderSalesView(); renderInteractions(); updateDashboard(); renderClients(); renderFollowUps();
  }

  function renderSalesView(){
    const salesList = $('#salesList');
    const map = new Map();

    clients.forEach(c => {
      const rows = sales.filter(s => s.clientId === c.id);
      const total = (Number(c.initialSales) || 0) + rows.reduce((sum, s) => sum + (Number(s.amount) || 0), 0);
      if (total > 0 || rows.length > 0) map.set(c.id, { client:c, rows, total });
    });

    if (map.size === 0){
      salesList.innerHTML = `
        <div class="empty-state">
          <div style="font-size:42px;opacity:.6">ð°</div>
          <p>No sales data available</p>
        </div>`;
      return;
    }

    const sorted = [...map.values()].sort((a,b) => b.total - a.total);
    salesList.innerHTML = sorted.map(({client:c, rows, total}) => `
      <div class="client-item">
        <div class="client-header">
          <div>
            <div class="client-name">${escapeHTML(fullNameOf(c))}</div>
            <div class="muted" style="margin-top:4px">Total Sales: <strong style="color:#2f855a">${fmtUSD.format(total)}</strong></div>
          </div>
        </div>
          ${Number(c.initialSales)>0 ? `
          <div style="padding:10px 0;border-bottom:1px solid #eee;display:flex;justify-content:space-between">
            <div style="font-weight:600">Initial Sales</div>
            <div style="font-weight:800;color:#2f855a">${fmtUSD.format(Number(c.initialSales) || 0)}</div>
          </div>` : ''}
        ${rows.sort((a,b)=>new Date(b.date)-new Date(a.date)).map(s => `
          <div style="padding:10px 0;border-bottom:1px solid #eee;display:flex;justify-content:space-between;align-items:center">
            <div>
              <div style="font-weight:600">${escapeHTML(s.description || 'Sale')}</div>
              <div class="muted" style="font-size:.85rem">${new Date(s.date).toLocaleDateString()}</div>
            </div>
            <div style="display:flex;align-items:center;gap:10px">
              <div style="font-weight:800;color:#2f855a">${fmtUSD.format(Number(s.amount) || 0)}</div>
              <button class="btn ghost"  data-action="edit-sale" data-id="${s.id}">Edit</button>
              <button class="btn danger" data-action="delete-sale" data-id="${s.id}">Delete</button>
            </div>
          </div>`).join('')}
      </div>
    `).join('');
  }

  // ---------- Follow Ups ----------
  function openFollowUpModal(prefillClientId=null, defaultNotes=''){
    const select = $('#followupClient');
    select.innerHTML = '<option value="">Select client...</option>' +
      clients.map(c => `<option value="${c.id}">${escapeHTML(fullNameOf(c))}</option>`).join('');
    const today = new Date().toISOString().slice(0,10);
    $('#followupDate').value = today;
    $('#followupNotes').value = defaultNotes || '';
    if (prefillClientId) select.value = prefillClientId;

    const modal = $('#followupModal');
    modal.classList.add('active');
    setTimeout(() => { modal.querySelector('input,select,textarea,button')?.focus(); }, 0);
  }
  function closeFollowUpModal(){ $('#followupModal').classList.remove('active'); $('#followupForm').reset(); }

  function saveFollowUp(e){
    e.preventDefault();
    const clientId = $('#followupClient').value;
    const date = $('#followupDate').value;
    if (!clientId || !date){ alert('Client and due date are required'); return; }
    followUps.push({
      id: Date.now().toString(),
      clientId, date,
      notes: $('#followupNotes').value.trim(),
      createdAt: new Date().toISOString(),
      completed: false, completedAt: null, type: 'manual'
    });
    saveData(); closeFollowUpModal(); renderFollowUps(); updateDashboard();
  }

  function renderFollowUps(){
    const todayStr = new Date().toISOString().slice(0,10);
    const today = new Date(todayStr);
    const pastDue = [], upcoming = [], future = [], emergency = [];

    // Split existing (pending) follow ups
    followUps.forEach(f => {
      if (f.completed) return;
      if (f.date < todayStr) pastDue.push(f);
      else if (f.date === todayStr || (new Date(f.date) - today) / 86400000 <= 14) upcoming.push(f);
      else future.push(f);
    });

    // Build 911 list (no interactions for 2+ months)
    const threshold = new Date(today);
    threshold.setMonth(threshold.getMonth() - 2);
    clients.forEach(c => {
      const lastIt = lastInteractionDate(c.id) || (c.createdAt ? new Date(c.createdAt) : null);
      if (!lastIt) return;
      if (lastIt < threshold) {
        emergency.push({ clientId: c.id, lastDate: lastIt });
      }
    });

    const byDateAsc = (a,b) => new Date(a.date) - new Date(b.date);
    $('#followupPastDue').innerHTML = pastDue.sort(byDateAsc).map(renderFollowUpRow).join('') || `<div class="muted">â</div>`;
    $('#followupUpcoming').innerHTML = upcoming.sort(byDateAsc).map(renderFollowUpRow).join('') || `<div class="muted">â</div>`;
    $('#followupFuture').innerHTML = future.sort(byDateAsc).map(renderFollowUpRow).join('') || `<div class="muted">â</div>`;
    $('#followup911').innerHTML = render911List(emergency) || `<div class="muted">â</div>`;
  }

  function renderFollowUpRow(f){
    const c = clients.find(x => x.id === f.clientId);
    const when = new Date(f.date).toLocaleDateString();
    const typeLabel = f.type === 'weekly' ? ' (Weekly)' : f.type === 'monthly' ? ' (Monthly)' : '';
    const isAuto = f.type !== 'manual';
    const autoIcon = isAuto ? 'ð¤ ' : '';
    return `
      <div class="followup-card">
        <div class="followup-top">
          <div class="followup-main">
            <div class="client-name">${escapeHTML(c ? fullNameOf(c) : 'Unknown Client')}</div>
            <div class="muted">${autoIcon}${when}${typeLabel}</div>
            ${f.notes ? `<div>${escapeHTML(f.notes)}</div>` : ''}
          </div>
        </div>
        <div class="card-actions">
          <button class="btn ${f.completed ? 'ghost':'primary'}" data-action="toggle-followup" data-id="${f.id}">${f.completed ? 'Reopen' : 'Mark Done'}</button>
          ${isAuto ? `<button class="btn danger" data-action="delete-followup" data-id="${f.id}">Delete</button>` : ''}
        </div>
      </div>`;
  }

  function render911List(items){
    if (!items.length) return '';
    const seen = new Set();
    return items.filter(x => {
      if (seen.has(x.clientId)) return false;
      seen.add(x.clientId); return true;
    }).sort((a,b)=>a.lastDate - b.lastDate).map(x => {
      const c = clients.find(cc => cc.id === x.clientId);
      const name = c ? fullNameOf(c) : 'Unknown Client';
      const lastStr = x.lastDate ? new Date(x.lastDate).toLocaleDateString() : 'â';
      const note = `URGENT: No interactions since ${lastStr}`;
      return `
        <div class="followup-card pill-911">
          <div class="followup-top">
            <div class="followup-main">
              <div class="client-name">ð¨ ${escapeHTML(name)}</div>
              <div class="muted">Last interaction: ${lastStr}</div>
              <div>No interactions for 2+ months â immediate outreach recommended.</div>
            </div>
          </div>
          <div class="card-actions">
            <button class="btn primary" data-action="create-followup-for-client" data-id="${x.clientId}" data-notes="${escapeHTML(note)}">Create FollowâUp</button>
          </div>
        </div>`;
    }).join('');
  }

  // ---------- Dashboard ----------
  function updateDashboard(){
    $('#totalClients').textContent = clients.length;
    $('#totalInteractions').textContent = interactions.length;
    const monthStart = new Date(); monthStart.setDate(1);
    const activeThisMonth = interactions.filter(i => new Date(i.date) >= monthStart).length;
    $('#activeThisMonth').textContent = activeThisMonth;
    const totalSales = clients.reduce((sum,c) => sum + (Number(c.initialSales)||0),0) +
      sales.reduce((sum,s) => sum + (Number(s.amount)||0),0);
    $('#totalSales').textContent = fmtUSD.format(totalSales);
    renderRecentActivity();
  }

  function renderRecentActivity(){
    const interWrap = $('#interactionActivityList');
    const salesWrap = $('#salesActivityList');

    if (interactions.length === 0){
      interWrap.innerHTML = `
        <div class="empty-state">
          <div style="font-size:42px;opacity:.6">ð¬</div>
          <p>No interactions yet</p>
        </div>`;
    } else {
      const items = [...interactions].sort((a,b)=>new Date(b.date)-new Date(a.date)).slice(0,6).map(i=>{
        const c = clients.find(x=>x.id===i.clientId);
        return `
          <div class="interaction-item">
            <div class="client-header" style="align-items:center">
              <div>
                <div class="client-name">${escapeHTML(c?fullNameOf(c):'Unknown Client')}</div>
                <div class="muted" style="margin-top:4px">${escapeHTML(i.type)} â¢ ${new Date(i.date).toLocaleDateString()}</div>
              </div>
            </div>
            ${i.notes ? `<div style="margin-top:8px">${escapeHTML(i.notes)}</div>`:''}
          </div>`;
      }).join('');
      interWrap.innerHTML = items;
    }

    if (sales.length === 0){
      salesWrap.innerHTML = `
        <div class="empty-state">
          <div style="font-size:42px;opacity:.6">ð°</div>
          <p>No sales yet</p>
        </div>`;
    } else {
      const items = [...sales].sort((a,b)=>new Date(b.date)-new Date(a.date)).slice(0,6).map(s=>{
        const c = clients.find(x=>x.id===s.clientId);
        return `
          <div class="interaction-item">
            <div class="client-header" style="align-items:center">
              <div>
                <div class="client-name">${escapeHTML(c?fullNameOf(c):'Unknown Client')}</div>
                <div class="muted" style="margin-top:4px">${new Date(s.date).toLocaleDateString()}</div>
              </div>
              <div style="font-weight:800;color:#2f855a">${fmtUSD.format(Number(s.amount)||0)}</div>
            </div>
            ${s.description ? `<div style="margin-top:8px">${escapeHTML(s.description)}</div>`:''}
          </div>`;
      }).join('');
      salesWrap.innerHTML = items;
    }
  }
</script>
</body>
</html>
