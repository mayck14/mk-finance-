<!DOCTYPE html><html lang="pt-BR"><head><meta charset="utf-8"><meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover"><title>MK Finance</title>
<link href="https://fonts.googleapis.com/css2?family=Manrope:wght@400;600;800&display=swap" rel="stylesheet">
<style>
:root{color-scheme:dark;--bg:#14161a;--sf:#1d2026;--ln:#2b2f38;--tx:#e9ebee;--mt:#8c94a1;--gn:#34d27b;--rd:#ff5d63;--bl:#6ea8ff;box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}
*{box-sizing:border-box}html{scroll-padding-top:env(safe-area-inset-top,0px)}
body{margin:0;background:var(--bg);color:var(--tx);font:400 15px/1.45 Manrope,system-ui,sans-serif}
aside{position:fixed;inset:0 auto 0 0;width:200px;padding:20px 12px;border-right:1px solid var(--ln);background:var(--bg)}
aside h1{font-size:18px;font-weight:800;margin:0 8px 18px;letter-spacing:.5px}aside h1 b{color:var(--gn)}
aside button{display:block;width:100%;text-align:left;background:none;border:0;color:var(--mt);padding:10px;border-radius:8px;font:600 14px Manrope,sans-serif;cursor:pointer}
aside button.on{background:var(--sf);color:var(--tx)}aside button i{font-style:normal;display:inline-block;width:22px}
main{margin-left:200px;padding:24px;max-width:1000px}
h2{font-size:22px;font-weight:800;margin:0 0 16px}h3{font-size:15px;margin:0 0 10px}
.g{display:grid;gap:12px;grid-template-columns:repeat(auto-fill,minmax(160px,1fr));margin-bottom:16px}
.c{background:var(--sf);border:1px solid var(--ln);border-radius:12px;padding:14px;margin-bottom:14px}.g .c{margin:0}
.k small{color:var(--mt);display:block}.k b{font-size:19px;font-weight:800}
.pos{color:var(--gn)}.neg{color:var(--rd)}.mt{color:var(--mt)}
label{display:block;font-size:12px;color:var(--mt)}
input,select,textarea{width:100%;margin-top:3px;background:var(--bg);color:var(--tx);border:1px solid var(--ln);border-radius:8px;padding:9px;font:inherit}
.f{display:grid;gap:10px;grid-template-columns:repeat(auto-fill,minmax(150px,1fr))}
.b{background:var(--gn);color:#06130b;border:0;border-radius:8px;padding:9px 14px;font:700 14px Manrope,sans-serif;cursor:pointer}
.b.s{background:var(--ln);color:var(--tx)}.b.x{background:none;color:var(--rd);padding:4px 8px}.b.sm{padding:4px 9px;font-size:12px}
.r{display:flex;gap:10px;align-items:center;justify-content:space-between;padding:9px 0;border-top:1px solid var(--ln)}.r:first-child{border-top:0}
.r>div:first-child{min-width:0;flex:1}.r small{color:var(--mt);display:block}
.bar{height:8px;background:var(--ln);border-radius:5px;overflow:hidden;margin-top:6px}.bar i{display:block;height:100%;background:var(--gn)}
.tabs{display:flex;gap:6px;margin-bottom:10px;flex-wrap:wrap}.al{border-left:3px solid var(--rd);padding:6px 10px;margin:6px 0;background:var(--bg);border-radius:4px}
.ok{border-color:var(--gn)}.err{color:var(--rd);margin:8px 0}svg{width:100%;height:auto;display:block}
@media(max-width:760px){aside{inset:auto 0 0 0;width:auto;display:flex;padding:4px 4px calc(4px + env(safe-area-inset-bottom,0px));border:0;border-top:1px solid var(--ln);z-index:5}
aside h1{display:none}aside button{text-align:center;padding:6px 0;font-size:10px}aside button i{display:block;width:auto;font-size:17px}
main{margin:0;padding:16px 14px 90px}}
@media print{aside,.np{display:none}main{margin:0}body{background:#fff;color:#000}.c{border-color:#999;background:#fff}}
@media(max-width:760px){.dk{display:none}}.out aside{display:none}.out main{margin:0 auto;padding:16px}#t{position:fixed;left:50%;bottom:80px;transform:translateX(-50%);background:var(--sf);border:1px solid var(--ln);padding:8px 14px;border-radius:8px;z-index:9;display:none;max-width:90%}
</style></head><body>
<aside id="nav"></aside><main id="v"></main><div id="t"></div>
<script>
/* ===== ARMAZENAMENTO LOCAL (IndexedDB): único ponto de contato com o banco ===== */
const COLS=['tx','biz','bl','inv','goals'];
let S={tx:[],biz:[],bl:[],inv:[],goals:[]},idb,snap={},q=Promise.resolve(),tt,memOnly=0;
const mk=c=>new Map(S[c].map(x=>[x.id,JSON.stringify(x)]));
const opn=()=>new Promise((ok,no)=>{const r=indexedDB.open('mkfinance',1);r.onupgradeneeded=()=>COLS.forEach(c=>r.result.createObjectStore(c,{keyPath:'id'}));r.onsuccess=()=>ok(r.result);r.onerror=()=>no(r.error)});
const req=r=>new Promise((ok,no)=>{r.onsuccess=()=>ok(r.result);r.onerror=()=>no(r.error)});
async function load(){for(const c of COLS){S[c]=await req(idb.transaction(c).objectStore(c).getAll());snap[c]=mk(c)}}
async function push(){const t=idb.transaction(COLS,'readwrite'),cur={};
 for(const c of COLS){const st=t.objectStore(c);cur[c]=mk(c);snap[c].forEach((_,id)=>{if(!cur[c].has(id))st.delete(id)});S[c].forEach(x=>{if(snap[c].get(x.id)!==cur[c].get(x.id))st.put(JSON.parse(JSON.stringify(x)))})}
 await new Promise((ok,no)=>{t.oncomplete=ok;t.onerror=t.onabort=()=>no(t.error)});COLS.forEach(c=>snap[c]=cur[c])}
const save=()=>{if(memOnly)return;q=q.then(push).then(()=>toast('Salvo')).catch(e=>toast('Não foi possível salvar: '+((e&&e.message)||'erro'),1))};
function toast(m,bad){const e=document.getElementById('t');e.textContent=m;e.style.color=bad?'var(--rd)':'var(--gn)';e.style.display='block';clearTimeout(tt);tt=setTimeout(()=>e.style.display='none',bad?5000:1200)}

const $=s=>document.querySelector(s),V=id=>$('#'+id).value,uid=()=>Date.now().toString(36)+Math.random().toString(36).slice(2,9);
const R=v=>(v||0).toLocaleString('pt-BR',{style:'currency',currency:'BRL'});
const esc=s=>String(s??'').replace(/[&<>"']/g,c=>({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[c]));
const num=v=>{v=parseFloat(String(v).replace(',','.'));return isFinite(v)?v:NaN};
const p2=n=>String(n).padStart(2,'0'),fmt=d=>d.getFullYear()+'-'+p2(d.getMonth()+1)+'-'+p2(d.getDate());
const today=()=>fmt(new Date()),D=s=>new Date(s+'T12:00'),add=(s,n)=>{const d=D(s);d.setDate(d.getDate()+n);return fmt(d)};
const wk=s=>add(s,-((D(s).getDay()+6)%7)),br=s=>s.split('-').reverse().join('/');
const sm=(a,f)=>a.reduce((x,t)=>x+f(t),0),pc=(a,b)=>b?Math.round(a/b*100):0;
const real=()=>S.tx.filter(t=>t.tipo!=='transf'),inc=l=>sm(l.filter(t=>t.tipo==='receita'),t=>t.valor),exp=l=>sm(l.filter(t=>t.tipo==='despesa'),t=>t.valor);
const CD=['Alimentação','Transporte','Educação','Saúde','Lazer','Compras','Investimentos','Contas fixas','Negócios','Outros'],CR=['Salário','Vendas','Serviços','Comissões','Rendimentos','Outros'];
const PG=['Pix','Dinheiro','Débito','Crédito','Boleto','Transferência'];
const catsFor=t=>t==='receita'?CR:t==='despesa'?CD:['Transferência entre contas'];
const inp=(id,l,t,v,x)=>`<label>${l}<input id="${id}" type="${t}" value="${esc(v)}" ${x||''}></label>`;
const sel=(id,l,o,v,x)=>`<label>${l}<select id="${id}" ${x||''}>${o.map(a=>{const[k,n]=Array.isArray(a)?a:[a,a];return`<option value="${esc(k)}"${k==v?' selected':''}>${esc(n)}</option>`}).join('')}</select></label>`;
function rng(p,s){if(p==='dia')return[s,s];if(p==='semana'){const a=wk(s);return[a,add(a,6)]}const d=D(s);
 if(p==='mes')return[fmt(new Date(d.getFullYear(),d.getMonth(),1)),fmt(new Date(d.getFullYear(),d.getMonth()+1,0))];return[d.getFullYear()+'-01-01',d.getFullYear()+'-12-31']}
function prv(p,s){const a=rng(p,s)[0];if(p==='dia')return add(a,-1);if(p==='semana')return add(a,-7);const d=D(a);return fmt(p==='mes'?new Date(d.getFullYear(),d.getMonth()-1,1):new Date(d.getFullYear()-1,0,1))}
const inR=(p,s)=>{const[a,b]=rng(p,s);return real().filter(t=>t.data>=a&&t.data<=b)};
function bars(p,n){const L=[],d0=new Date();
 for(let i=n-1;i>=0;i--){const k=p==='dia'?add(today(),-i):p==='semana'?add(wk(today()),-7*i):p==='mes'?fmt(new Date(d0.getFullYear(),d0.getMonth()-i,1)):(d0.getFullYear()-i)+'-01-01';
  const l=inR(p,k);L.push({k,r:inc(l),d:exp(l)})}
 const mx=Math.max(1,...L.flatMap(x=>[x.r,x.d]));if(!L.some(x=>x.r||x.d))return'<p class="mt">Sem dados no período. Registre movimentações para ver o gráfico.</p>';
 const W=640,H=200,w=W/n;let o=`<svg viewBox="0 0 ${W} ${H+22}" role="img" aria-label="Receitas e despesas">`;
 L.forEach((x,i)=>{const hr=x.r/mx*H,hd=x.d/mx*H,lb=p==='ano'?x.k.slice(0,4):p==='mes'?x.k.slice(5,7)+'/'+x.k.slice(2,4):x.k.slice(8)+'/'+x.k.slice(5,7);
  o+=`<rect x="${i*w+w*.12}" y="${H-hr}" width="${w*.36}" height="${hr}" rx="3" fill="#34d27b"><title>${lb} receitas ${R(x.r)}</title></rect><rect x="${i*w+w*.5}" y="${H-hd}" width="${w*.36}" height="${hd}" rx="3" fill="#ff5d63"><title>${lb} despesas ${R(x.d)}</title></rect><text x="${i*w+w/2}" y="${H+15}" fill="#8c94a1" font-size="11" text-anchor="middle">${lb}</text>`});
 return o+'</svg><small class="mt">Verde: receitas · Vermelho: despesas</small>'}
const kpi=(l,v,c)=>`<div class="c k"><small>${l}</small><b class="${c||''}">${v}</b></div>`;
const tabs=(a,cur,fn)=>`<div class="tabs np">${a.map(([k,n])=>`<button class="b sm ${k==cur?'':'s'}" onclick="${fn}('${k}')">${n}</button>`).join('')}</div>`;
let view='painel',cp='mes',ed=null,dl=null,F={from:'',to:'',cat:'',tipo:'',q:''},am=today().slice(0,7),rp='mes',rd=today();
const NAV=[['painel','▦','Painel'],['mov','⇄','Movim.'],['analise','◔','Análise'],['neg','▣','Negócios'],['inv','↗','Investir'],['metas','◎','Metas'],['rel','☰','Relatórios']];
function go(v){view=v;ed=null;dl=null;render()}
function render(){$('#nav').innerHTML='<h1>MK <b>FINANCE</b></h1>'+NAV.map(n=>`<button class="${n[0]==view?'on':''}" onclick="go('${n[0]}')"><i>${n[1]}</i>${n[2]}</button>`).join('');
 $('#v').innerHTML=(memOnly?'<div class="al">O navegador bloqueou o armazenamento local: os dados NÃO estão sendo salvos. Baixe um backup antes de sair.</div>':'')+({painel:vPainel,mov:vMov,analise:vAnalise,neg:vNeg,inv:vInv,metas:vMetas,rel:vRel})[view]();scrollTo(0,0)}
function del(c,id){if(dl===c+id){S[c]=S[c].filter(x=>x.id!==id);if(c==='biz')S.bl=S.bl.filter(x=>x.biz!==id);dl=null;save()}else dl=c+id;const y=scrollY;render();scrollTo(0,y)}
const delB=(c,id)=>`<button class="b x" onclick="del('${c}','${id}')">${dl===c+id?'Confirmar?':'Excluir'}</button>`;
/* PAINEL */
function vPainel(){const m=today().slice(0,7),l=inR('mes',today()),e=inc(l),d=exp(l),all=real(),ok=t=>t.status!=='pendente';
 const saldo=inc(all.filter(ok))-exp(all.filter(ok)),pend=(t)=>sm(all.filter(x=>x.tipo===t&&x.status==='pendente'),x=>x.valor);
 const invT=sm(S.inv,i=>i.atual!=null?i.atual:i.ini+sm(i.ap||[],a=>a.v)),res=sm(S.goals,g=>g.salvo);
 return`<h2>Painel</h2><div class="g">${kpi('Saldo disponível',R(saldo),saldo<0?'neg':'')}${kpi('Entradas no mês',R(e),'pos')}${kpi('Despesas no mês',R(d),'neg')}${kpi('Lucro líquido',R(e-d),e-d<0?'neg':'pos')}${kpi('Percentual de lucro',pc(e-d,e)+'%')}${kpi('Despesas / receitas',pc(d,e)+'%')}${kpi('Total investido',R(invT))}${kpi('Dinheiro reservado',R(res))}${kpi('Contas a pagar',R(pend('despesa')),'neg')}${kpi('Contas a receber',R(pend('receita')),'pos')}</div>
 <div class="c"><h3>Evolução financeira</h3>${tabs([['dia','Dia'],['semana','Semana'],['mes','Mês'],['ano','Ano']],cp,'setCp')}${bars(cp,{dia:14,semana:8,mes:12,ano:5}[cp])}</div>
 ${S.tx.length?'':'<div class="c">Nenhum dado ainda. Comece em <b>Movimentações</b>: todos os números aparecem conforme você registra.</div>'}`}
function setCp(k){cp=k;render()}
/* MOVIMENTAÇÕES */
function fillCats(){$('#cat').innerHTML=catsFor(V('tipo')).map(c=>`<option>${c}</option>`).join('')}
function vMov(){const e=S.tx.find(t=>t.id===ed)||{tipo:'despesa',data:today(),status:'pago',forma:'Pix',cat:'Alimentação'};
 let l=S.tx.filter(t=>(!F.from||t.data>=F.from)&&(!F.to||t.data<=F.to)&&(!F.cat||t.cat===F.cat)&&(!F.tipo||t.tipo===F.tipo)&&(!F.q||(t.desc+t.obs).toLowerCase().includes(F.q.toLowerCase()))).sort((a,b)=>b.data.localeCompare(a.data));
 return`<h2>Movimentações</h2><div class="c"><h3>${ed?'Editar':'Nova'} movimentação</h3><div class="f">${inp('d','Descrição','text',e.desc||'')}${inp('vl','Valor (R$)','number',e.valor||'','step="0.01" min="0" inputmode="decimal"')}${inp('dt','Data','date',e.data)}
 ${sel('tipo','Tipo',[['despesa','Despesa'],['receita','Receita'],['transf','Transferência entre contas']],e.tipo,'onchange="fillCats()"')}${sel('cat','Categoria',catsFor(e.tipo),e.cat)}${sel('fp','Forma de pagamento',PG,e.forma)}${sel('st','Situação',[['pago','Pago / recebido'],['pendente','Pendente']],e.status)}${inp('ob','Observações','text',e.obs||'')}</div>
 <div id="err" class="err"></div><button class="b" onclick="saveTx()">${ed?'Salvar alterações':'Registrar'}</button> ${ed?'<button class="b s" onclick="go(\'mov\')">Cancelar</button>':''}<p class="mt" style="font-size:12px;margin:8px 0 0">Transferências entre suas contas não entram como receita nem despesa.</p></div>
 <div class="c"><h3>Filtros</h3><div class="f">${inp('f1','De','date',F.from,'onchange="setF()"')}${inp('f2','Até','date',F.to,'onchange="setF()"')}${sel('f3','Categoria',[['','Todas'],...[...new Set([...CD,...CR])]],F.cat,'onchange="setF()"')}${sel('f4','Tipo',[['','Todos'],['receita','Receitas'],['despesa','Despesas'],['transf','Transferências']],F.tipo,'onchange="setF()"')}${inp('f5','Buscar','text',F.q,'onchange="setF()"')}</div></div>
 <div class="c">${l.length?l.map(t=>`<div class="r"><div>${esc(t.desc)}<small>${br(t.data)} · ${esc(t.cat)} · ${esc(t.forma)}${t.status==='pendente'?' · <b class="neg">pendente</b>':''}${t.obs?' · '+esc(t.obs):''}</small></div><b class="${t.tipo==='receita'?'pos':t.tipo==='despesa'?'neg':'mt'}">${t.tipo==='despesa'?'−':t.tipo==='receita'?'+':''}${R(t.valor)}</b><div class="np">${t.status==='pendente'?`<button class="b sm" onclick="pay('${t.id}')">Pagar</button> `:''}<button class="b s sm" onclick="ed='${t.id}';render()">Editar</button>${delB('tx',t.id)}</div></div>`).join(''):'<p class="mt">Nenhuma movimentação encontrada.</p>'}</div>`}
function setF(){F={from:V('f1'),to:V('f2'),cat:V('f3'),tipo:V('f4'),q:V('f5')};render()}
function pay(id){S.tx.find(t=>t.id===id).status='pago';save();render()}
function saveTx(){const v=num(V('vl')),o={desc:V('d').trim(),valor:v,data:V('dt'),tipo:V('tipo'),cat:V('cat'),forma:V('fp'),status:V('st'),obs:V('ob').trim()};
 if(!o.desc)return $('#err').textContent='Informe uma descrição.';if(!(v>0))return $('#err').textContent='Informe um valor maior que zero.';if(!o.data)return $('#err').textContent='Informe a data.';
 if(ed)Object.assign(S.tx.find(t=>t.id===ed),o);else S.tx.push({id:uid(),...o});save();ed=null;render()}
/* ANÁLISE */
const grp=(l,t)=>{const m={};l.filter(x=>x.tipo===t).forEach(x=>m[x.cat]=(m[x.cat]||0)+x.valor);return Object.entries(m).sort((a,b)=>b[1]-a[1])};
function vAnalise(){const s=am+'-01',l=inR('mes',s),pl=inR('mes',prv('mes',s)),e=inc(l),d=exp(l),pe=inc(pl),pd=exp(pl),gd=grp(l,'despesa'),gp=Object.fromEntries(grp(pl,'despesa')),gr=grp(l,'receita'),I=[],A=[];
 if(!l.length)I.push('Sem movimentações neste mês para analisar.');else{
 if(pd>0){const v=Math.round((d-pd)/pd*100);I.push(`Suas despesas ${v>=0?'aumentaram':'diminuíram'} ${Math.abs(v)}% em comparação ao mês anterior.`)}
 if(pl.length&&e-d<pe-pd)I.push('Seu lucro líquido diminuiu em relação ao mês anterior.');else if(pl.length&&e-d>pe-pd)I.push('Seu lucro líquido aumentou em relação ao mês anterior.');
 if(e-d<0)I.push(`Você gastou ${R(d-e)} a mais do que recebeu neste mês.`);
 if(e>0)I.push(`As despesas consomem ${pc(d,e)}% das suas receitas.`);
 if(gr[0])I.push(`Sua maior fonte de renda neste mês é ${gr[0][0]} (${R(gr[0][1])}).`);
 if(gd[0]){I.push(`Sua maior fonte de despesa é ${gd[0][0]} (${R(gd[0][1])}, ${pc(gd[0][1],d)}% dos gastos).`);I.push(`Reduzir 10% de ${gd[0][0]} economizaria ${R(gd[0][1]*.1)} por mês.`)}}
 gd.forEach(([c,v])=>{const p=gp[c]||0;if(p>0&&v>p*1.3&&v-p>=1)A.push(`${c} subiu ${Math.round((v-p)/p*100)}% (de ${R(p)} para ${R(v)}).`);else if(!p&&pd>0&&v>pd*.1)A.push(`${c} é uma categoria nova com ${R(v)} neste mês.`)});
 return`<h2>Análise de lucros e prejuízos</h2><div class="c">${inp('am','Mês','month',am,'onchange="am=V(\'am\');render()"')}</div>
 <div class="g">${kpi('Receitas',R(e),'pos')}${kpi('Despesas',R(d),'neg')}${kpi('Resultado',R(e-d),e-d<0?'neg':'pos')}</div>
 <div class="c"><h3>Assistente financeiro</h3>${I.map(x=>`<div class="al ok">${esc(x)}</div>`).join('')}${A.map(x=>`<div class="al">Alerta: ${esc(x)}</div>`).join('')}<small class="mt">Baseado apenas nos seus registros.</small></div>
 <div class="c"><h3>Ranking de despesas por categoria</h3>${gd.length?gd.map(([c,v])=>`<div class="r" style="display:block"><div style="display:flex;justify-content:space-between"><span>${esc(c)}</span><b class="neg">${R(v)} · ${pc(v,d)}%</b></div><div class="bar"><i style="width:${pc(v,gd[0][1])}%;background:var(--rd)"></i></div></div>`).join(''):'<p class="mt">Sem despesas no mês.</p>'}</div>
 <div class="c"><h3>Atividades que mais geram receita</h3>${gr.length?gr.map(([c,v])=>`<div class="r"><span>${esc(c)}</span><b class="pos">${R(v)}</b></div>`).join(''):'<p class="mt">Sem receitas no mês.</p>'}</div>
 <div class="c"><h3>Receitas × despesas (6 meses)</h3>${bars('mes',6)}</div>`}
/* NEGÓCIOS */
const BK={venda:'Venda',custo:'Custo de produção',oper:'Despesa operacional',invest:'Investimento no negócio'};
function bm(b){const l=S.bl.filter(x=>x.biz===b.id),s=k=>sm(l.filter(x=>x.k===k),x=>x.v),fat=s('venda'),bru=fat-s('custo'),liq=bru-s('oper');return{fat,bru,liq,mg:pc(liq,fat),inv:s('invest'),l}}
function vNeg(){return`<h2>Negócios</h2><div class="c"><h3>Novo negócio</h3><div class="f">${inp('bn','Nome','text','')}</div><div id="err" class="err"></div><button class="b" onclick="addBiz()">Cadastrar</button></div>
 ${S.biz.length?`<div class="c"><h3>Comparativo</h3>${S.biz.map(b=>{const m=bm(b);return`<div class="r"><div>${esc(b.nome)}<small>Faturamento ${R(m.fat)} · margem ${m.mg}%</small></div><b class="${m.liq<0?'neg':'pos'}">${R(m.liq)}</b></div>`}).join('')}</div>`:'<div class="c mt">Cadastre seu primeiro negócio para registrar vendas e custos.</div>'}
 ${S.biz.map(b=>{const m=bm(b);return`<div class="c"><div class="r"><h3 style="margin:0">${esc(b.nome)}</h3>${delB('biz',b.id)}</div><div class="g">${kpi('Faturamento',R(m.fat))}${kpi('Lucro bruto',R(m.bru),m.bru<0?'neg':'pos')}${kpi('Lucro líquido',R(m.liq),m.liq<0?'neg':'pos')}${kpi('Margem',m.mg+'%')}${kpi('Investido',R(m.inv))}</div>
 <div class="f">${sel('k'+b.id,'Tipo',Object.entries(BK),'venda')}${inp('v'+b.id,'Valor (R$)','number','','step="0.01" min="0"')}${inp('t'+b.id,'Data','date',today())}${inp('n'+b.id,'Descrição','text','')}</div><p><button class="b" onclick="addBl('${b.id}')">Registrar</button></p>
 ${m.l.sort((a,b)=>b.d.localeCompare(a.d)).slice(0,8).map(x=>`<div class="r"><div>${esc(x.n||BK[x.k])}<small>${br(x.d)} · ${BK[x.k]}</small></div><b>${R(x.v)}</b>${delB('bl',x.id)}</div>`).join('')}</div>`}).join('')}`}
function addBiz(){const n=V('bn').trim();if(!n)return $('#err').textContent='Informe o nome.';S.biz.push({id:uid(),nome:n});save();render()}
function addBl(b){const v=num(V('v'+b));if(!(v>0)||!V('t'+b))return alert('Informe valor e data.');S.bl.push({id:uid(),biz:b,k:V('k'+b),v,d:V('t'+b),n:V('n'+b).trim()});save();render()}
/* INVESTIMENTOS */
const ia=i=>i.ini+sm(i.ap||[],a=>a.v);
function vInv(){const T=sm(S.inv,ia),A=sm(S.inv,i=>i.atual!=null?i.atual:ia(i));
 return`<h2>Investimentos e reservas</h2><div class="g">${kpi('Total aportado',R(T))}${kpi('Patrimônio informado',R(A))}${kpi('Resultado',R(A-T),A-T<0?'neg':'pos')}</div>
 <div class="c"><h3>Novo investimento</h3><div class="f">${inp('in','Nome','text','')}${inp('ii','Instituição','text','')}${inp('iv','Valor inicial (R$)','number','','step="0.01" min="0"')}${inp('id','Data','date',today())}${inp('io','Objetivo','text','')}${inp('ir','Valor atual informado (opcional)','number','','step="0.01"')}</div><div id="err" class="err"></div><button class="b" onclick="addInv()">Cadastrar</button><p class="mt" style="font-size:12px">A rentabilidade vem apenas do valor atual que você informar.</p></div>
 ${S.inv.map(i=>{const a=i.atual!=null?i.atual:ia(i),r=ia(i)?Math.round((a-ia(i))/ia(i)*1000)/10:0;return`<div class="c"><div class="r"><div><b>${esc(i.n
