<h3 id="apontar-o-domínio-para-o-bucket-s3">Apontar o domínio para o Bucket S3</h3>
<p>A peça final do nosso projeto é criar um registro DNS que vai redirecionar o tráfego do domínio para a distribuição do CloudFront.</p>
<ul>
<li>No Route 53, acesse a Zona hospedada e clique em “<strong>Criar registro”</strong></li>
<li>Em Tipo de registro, selecione o tipo A e marque a opção “<em>Alias</em>” - os registros do tipo <em>alias</em> permitem rotear o tráfego para serviços internos que provisionamos na AWS</li>
<li>Em seguida, em <strong>Rotear o tráfego para</strong> selecione “<em>Alias para distribuição do CloudFront</em>”. Vai aparecer a distribuição que criamos na lista.</li>
<li>No campo da política de roteamento, mantenha o “<em>Roteamento simples</em>” - No Roteamento simples, nós encaminhamos o tráfego para um único recurso</li>
<li>Clique em “ <strong>Criar registros”.</strong></li>
</ul>
<p>Agora, basta aguardar a propagação dos registros DNS. Não deve demorar muito. Em poucos minutos, você conseguirá acessar o site pelo domínio.</p>

