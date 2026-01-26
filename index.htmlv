<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Portal Oficial de Reembolso</title>
<style>
:root{
  --border:#e5e7eb;--muted:#6b7280;--blue:#2563eb;--green:#16a34a;
  --green-soft:#ecfdf5;--blue-soft:#eff6ff;--red:#dc2626;--orange:#f59e0b;
}
*{box-sizing:border-box}
body{margin:0;background:#f3f5f9;font-family:Arial,Helvetica,sans-serif;color:#1f2937}
.app{max-width:980px;margin:40px auto;background:#fff;border-radius:14px;box-shadow:0 10px 30px rgba(0,0,0,.08)}
.header{padding:18px 24px;border-bottom:1px solid var(--border);display:flex;justify-content:space-between}
.header h1{margin:0;font-size:18px}
.header small{color:var(--muted)}
.content{padding:24px}
.hidden{display:none}

/* proteção texto */
.wrap{max-width:100%;overflow-wrap:anywhere;word-break:break-all;white-space:normal}

/* cards */
.card{border:1px solid var(--border);border-radius:10px;padding:14px 16px;margin-bottom:12px}
.card.green{border-left:4px solid var(--green)}
.card.red{border-left:4px solid var(--red)}
.card.blue{border-left:4px solid var(--blue)}
.card.orange{border-left:4px solid var(--orange);background:#fffbeb}

/* botões */
.actions{display:flex;gap:12px;margin-top:20px}
button{flex:1;padding:14px;border-radius:10px;border:none;font-size:15px;cursor:pointer}
button.primary{background:var(--blue);color:#fff}
button:disabled{opacity:.6;cursor:not-allowed}

/* etapa 2 */
label{font-weight:600;display:block;margin:14px 0 6px}
textarea{width:100%;min-height:180px;padding:14px;border-radius:10px;border:1px solid var(--border)}
.counter{display:flex;justify-content:space-between;font-size:12px}
.counter .min{color:var(--red)}
.counter .ok{color:var(--green);font-weight:600}
.counter .count{color:var(--muted)}
.notice{margin-top:14px;border-left:4px solid var(--orange);background:#fffbeb;padding:14px;border-radius:8px}

/* etapa final */
.success{border-left:4px solid var(--green);background:var(--green-soft);padding:16px;border-radius:12px}
.badge{display:inline-flex;gap:6px;background:#dcfce7;color:#166534;padding:6px 12px;border-radius:999px;font-size:12px;margin:6px 0}
.grid{display:grid;grid-template-columns:repeat(2,1fr);gap:12px;margin:16px 0}
.box{border:1px solid var(--border);border-radius:12px;padding:14px}
.box span{font-size:12px;color:var(--muted);display:block}
.steps{display:grid;grid-template-columns:repeat(4,1fr);gap:12px;margin:20px 0}
.step{border:1px solid var(--border);border-radius:12px;padding:12px;font-size:13px}
.step.done{background:var(--green-soft)}
.step.progress{background:var(--blue-soft)}
.step.wait{background:#f9fafb}
.info{border-left:4px solid var(--blue);background:#f8fafc;padding:16px;border-radius:10px;margin-bottom:16px}
.summary{border:1px solid var(--border);border-radius:12px;padding:14px;margin-bottom:16px}
.warning{border-left:4px solid var(--orange);background:#fffbeb;padding:14px;border-radius:10px}

.footer{padding:16px;text-align:center;font-size:12px;color:var(--muted);border-top:1px solid var(--border)}
.footer a{color:var(--blue);text-decoration:none}
</style>
</head>
<body>

<div class="app">
  <div class="header">
    <h1>✔️ Portal Oficial de Reembolso</h1>
    <small>Última atualização: 2025</small>
  </div>

  <!-- ETAPA 1 -->
  <section id="s1" class="content">
    <h3>⚖️ Antes de prosseguir</h3>
    <div class="card green"><b>Solicitações são feitas exclusivamente por este formulário oficial.</b><br>Garante rastreabilidade, conformidade e prazo de análise previsível.</div>
    <div class="card red"><b>Pedidos abertos no banco/cartão serão negados.</b><br>Aberturas externas podem gerar retenção do valor e atrasos por análise do emissor.</div>
    <div class="card blue"><b>Evite transtornos.</b><br>Na próxima etapa você informará seus dados e anexará o comprovante da compra.</div>
    <div class="card orange"><b>⚠️ Importante</b>
      <ul>
        <li>Congelamento temporário do valor pode ocorrer fora do canal oficial;</li>
        <li>Contas podem ser analisadas e bloqueadas preventivamente pelo emissor;</li>
        <li>O descumprimento do fluxo pode implicar perda do direito ao reembolso.</li>
      </ul>
    </div>
    <div class="actions">
      <button class="primary" onclick="go(2)">Entendi e Continuar</button>
    </div>
  </section>

  <!-- ETAPA 2 -->
  <section id="s2" class="content hidden">
    <h3>📝 Justificativa do Pedido</h3>
    <label>Sua justificativa</label>
    <textarea id="just"></textarea>
    <div class="counter">
      <span id="minText" class="min">Mínimo recomendado: 120 caracteres</span>
      <span class="count" id="count">0 / 2000</span>
    </div>
    <button id="btn" class="primary" disabled onclick="go(3)">Solicitar reembolso</button>
    <div class="notice"><b>Atenção:</b> ao prosseguir você será redirecionado(a) para a próxima etapa do fluxo.</div>
  </section>

  <!-- ETAPA FINAL -->
  <section id="s3" class="content hidden">
    <div class="success">
      <b>Solicitação enviada com sucesso</b>
      <div class="badge">🟢 Em análise pela equipe</div>
      <div style="font-size:13px">Prazo estimado para o estorno: <b>5 a 7 dias úteis</b> após aprovação interna.</div>
    </div>

    <div class="grid">
      <div class="box wrap"><span>Protocolo</span><b>PR-20260126005841-J46RDX</b></div>
      <div class="box wrap"><span>Canal de contato</span>Enviaremos atualizações por e-mail</div>
      <div class="box wrap"><span>Recebido em</span>26/01/2026, 00:58</div>
      <div class="box wrap"><span>Situação</span>Em análise</div>
    </div>

    <div class="steps">
      <div class="step done">Etapa 1<br>Solicitação enviada<br><small>Concluída</small></div>
      <div class="step progress">Etapa 2<br>Análise da justificativa<br><small>Em andamento</small></div>
      <div class="step wait">Etapa 3<br>Solicitação de estorno<br><small>Próximo</small></div>
      <div class="step wait">Etapa 4<br>Confirmação ao cliente<br><small>Aguardando</small></div>
    </div>

    <div class="info"><b>O que acontece agora?</b><br>Nossa equipe fará a triagem da justificativa e encaminhará o pedido de estorno ao emissor do pagamento. Você receberá atualizações por e-mail.</div>

    <div class="summary wrap"><span>Resumo da justificativa</span><div id="resumo" style="margin-top:6px"></div></div>

    <div class="warning wrap"><b>Importante:</b> o prazo de crédito no extrato pode depender do emissor do cartão, banco ou carteira utilizada. Em caso de dúvidas, fale com <a href="mailto:suporte@private.com">suporte@private.com</a>.</div>
  </section>

  <div class="footer">
    Dúvidas? Contato oficial:
    <a href="mailto:suporte@private.com">suporte@private.com</a>
    · Política de Privacidade · Termos de Uso
    <br>© 2025 Sua Empresa. Todos os direitos reservados.
  </div>
</div>

<script>
function go(n){
  document.querySelectorAll("section").forEach(s=>s.classList.add("hidden"));
  document.getElementById("s"+n).classList.remove("hidden");
  if(n===3){
    document.getElementById("resumo").innerText = document.getElementById("just").value;
  }
}
const just=document.getElementById("just");
const count=document.getElementById("count");
const btn=document.getElementById("btn");
const minText=document.getElementById("minText");
just.addEventListener("input",()=>{
  const n=just.value.length;
  count.textContent=n+" / 2000";
  if(n>=120){
    btn.disabled=false;
    minText.textContent="✔ Pronto para enviar";
    minText.className="ok";
  }else{
    btn.disabled=true;
    minText.textContent="Mínimo recomendado: 120 caracteres";
    minText.className="min";
  }
});
</script>

</body>
</html>
