<h3 id="criando-um-certificado-ssl-no-aws-certificate-manager">Criando um certificado SSL no AWS Certificate Manager</h3>
<p>Um dos requisitos do nosso projeto é que ele suporte requisições seguras via HTTPS. Para permitir isso, primeiro devemos emitir um certificado SSL/TLS via <strong>AWS Certificate Manager</strong>.</p>
<p>O Certificate Manager é um serviço que permite a criação, gerenciamento e renovação de certificados SSL/TLS.</p>
<ul>
<li>Pesquise por <em>Certificate Manager</em> na console AWS</li>
<li>Verifique se a sua localização esteja em Norte da Virgínia (us-east-1). Se não estiver, altere para ela</li>
<li>Clique em “<em><strong>Solicitar um certificado</strong></em>”</li>
<li>Em tipo de certificado, deverá estar marcada a opção <em><strong>Solicitar um certificado público</strong></em>. Clique em “<em>Próximo</em>”.</li>
<li>Em <strong>Nomes de domínio</strong> forneça o nome do seu domínio</li>
<li>Em <strong>Método de validação</strong>: escolha o método de validação por DNS</li>
<li>Em <strong>Algoritmo chave</strong> mantenha como RSA 2048. Clique em “<em><strong>Solicitar</strong></em>”</li>
</ul>
<p>Como ele é um domínio registrado na AWS, haverá a opção Criar registros no Route53 - clique nela. Selecione o seu domínio e, em seguida, clique em “Criar registros”. Se tudo ocorreu bem, você terá uma mensagem de registro criado com êxito.</p>

