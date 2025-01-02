<h3 id="criar-uma-zona-hospedada-hosted-zone-no-route-53">Criar uma zona hospedada (hosted zone) no Route 53</h3>
<p>Se você optar por registrar seu domínio na AWS, a sua zona hospedada é criada automaticamente. Nesse caso, você não precisa fazer nada.</p>
<p>Caso você utilize um domínio registrado fora da AWS, vai precisar criar uma Zona Hospedada (<em>Hosted zone</em>).</p>
<p>Nesse caso, acesse a console AWS:</p>
<ul>
<li>Procure por Route 53</li>
<li>No painel, entre na opção Zonas hospedadas -&gt; clique em <em><strong>Criar zona hospedada</strong></em></li>
<li>Insira o domínio no campo <em>Nome do domínio</em> e deixe a opção <em>Zona hospedada pública</em> marcada. Clique em <em><strong>Criar zona hospedada</strong></em></li>
<li>A zona será criada com dois registros DNS: um do tipo NS que possui 4 valores, e outro do tipo SOA. Pegue os valores dos registros do tipo NS, copie e salve em um bloco de notas para facilitar o processo.</li>
<li>No painel DNS do seu domínio, ou seja, onde você registrou você deverá configurar os registros NS para os da AWS.</li>
</ul>

