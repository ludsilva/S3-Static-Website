<h3 id="criando-uma-distribuição-do-cloudfront">Criando uma distribuição do CloudFront</h3>
<p>Agora, vamos criar nossa distribuição de conteúdo (CND) no CloudFront.</p>
<ul>
<li>Acesse a console AWS e busque pelo CloudFront. Clique em <em><strong>Criar distribuição</strong></em> (<em>Create distribution)</em></li>
<li>Em <em>Origin domain</em>, você vai escolher o Bucket S3 em que os arquivos do Website - o CloudFront vai sugerir que você indique o <em>endpoint</em> do website, mas não faça isso</li>
<li>Em <em>Origin access,</em> marque a opção <em>Origin access control settings</em>, e depois clique no botão <em>Criar nova OAC</em></li>
<li>Um pop-up vai abrir para configurar o controle de acesso, apenas clique em <em>Criar (create)</em></li>
<li>Em Viewer marque <em>Redirect HTTP to HTTPS</em> (Redirecione acessos HTTP para HTTPS)</li>
<li>Cache policy and origin request policy (recommended): selecione <em>CachingDisabled</em></li>
<li>Mais abaixo, em <strong>Web Application</strong> <strong>Firewall (WAF)</strong>, marque a opção para <em>Não habilitar nenhuma proteção de segurança (Do not enable security protections)</em></li>
<li>Em <em>Settings</em> -&gt; na opção <em>Alternate domain name</em>, escolha Add item e preencha com seu domínio (no meu caso, é cloudtutorials.click)</li>
<li>Em <strong>Custom SSL certificate</strong>, escolha o certificado SSL criado no passo anterior</li>
<li>Na opção <em><strong>Default root object</strong></em> (Objeto raiz padrão), digite index.html</li>
<li>Crie a distribuição.</li>
</ul>
<p>Você verá que ao criar a distribuição, uma política de S3 será criada também. Copie a política, e substitua a que está no seu bucket por esta nova.</p>

