<h3 id="subindo-um-website-estático-no-s3">Subindo um Website estático no S3</h3>
<p>Agora que já temos um domínio em mãos, vamos começar a criar a estrutura de hospedagem do site. Para isso, você deve acessar a console AWS e buscar pelo S3.</p>
<p>No S3, você deverá criar um Bucket S3 para subir os arquivos do website. Para isso, clique no botão “<strong><em>Criar bucket</em></strong>” e preencher as informações:</p>
<ul>
<li><strong>Nome do bucket</strong>: defina um nome para o seu bucket</li>
<li><strong>Região AWS</strong>: Norte da Virgínia (us-east-1)</li>
<li><strong>Tipo de Bucket</strong>: Propósito geral</li>
<li>Ao criar o Bucket, desmarque a opção “<em>Bloquear todo o acesso público</em>” para que ele fique disponível na internet. Depois, desça até o final da página e clique em <em>Criar bucket</em></li>
</ul>
<p><strong>Carregar arquivos</strong></p>
<ul>
<li>Acesse o bucket e clique em “<em><strong>Carregar</strong></em>” para subir os arquivos do website</li>
</ul>
<p><strong>Alterar permissões</strong></p>
<ul>
<li>Em seguida, vá para -&gt; Permissões e vá até <strong>Política do bucket</strong>. Clique em <em>editar</em> e cole a seguinte política* e clique em <em><strong>Salvar alterações</strong></em>:<br>
<code>{ "Version": "2012-10-17", "Statement": [ { "Sid": "PublicReadGetObject", "Effect": "Allow", "Principal": "*", "Action": [ "s3:GetObject" ], "Resource": [ "arn:aws:s3:::Nome-do-Bucket/*" ] } ] }</code></li>
</ul>
<p>Lembre-se de mudar <em>Nome-do-Bucket</em> para o nome do seu bucket S3. Clique em <em><strong>Salvar alterações</strong></em></p>
<p><strong>Website estático</strong></p>
<ul>
<li>Por fim, vá até Propriedades -&gt; desça até a opção Hospedagem de site estático -&gt; clique em <em>editar</em>. Habilite a opção de hospedagem de site estático e aponte a página <em>index.html</em> como documento de índice. Clique em <em><strong>Editar hospedagem de site estático</strong></em></li>
<li>Marque a opção <em>Ativar</em>; em <strong>Tipo de hospedagem</strong> marque <em>Hospedar um site estático</em>; em <strong>Documento de índice</strong> indique o <em>index.html</em></li>
<li>Salve as configurações e acesse o endpoint gerado.</li>
</ul>

