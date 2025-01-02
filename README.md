<h1 id="aws-s3-static-website">AWS S3 Static Website</h1>
<p>Este projeto tem como objetivo apresentar o deploy de um site estático na AWS, com o intuito de servir como um tutorial para aqueles que estão dando seus primeiros passos na Computação em Nuvem.</p>
<h2 id="requisitos">Requisitos</h2>
<p>Os requisitos do projeto são:</p>
<ul>
<li>Um website estático hospedado na AWS com armazenamento durável;</li>
<li>Ter segurança e aceitar conexões HTTPS;</li>
<li>Aceitar requisições do tipo GET e HEAD;</li>
<li>Melhor desempenho e entrega para os usuários utilizando rede de entrega de conteúdo.</li>
</ul>
<h2 id="arquitetura">Arquitetura</h2>
<p>O diagrama de arquitetura de implantação do sistema nos ajuda a visualizar como tudo funciona.</p>
<p>[IMAGEM]</p>
<p>Os arquivos do site estão hospedados em um bucket no Amazon S3. O Route 53 faz o serviço de gerenciamento de DNS para o domínio do site. Além disso, temos um certificado SSL gerado com o Amazon Certificate Manager (ACM), a fim de garantir a segurança e criptografia através de requisições HTTPS. E o CloudFront para a entrega rápida dos conteúdos utilizando os Pontos de Presença (<em>Edge Locations</em>) da AWS.</p>
<p>Basicamente, o usuário digita a URL no navegador e a requisição passa pela Zona de DNS do domínio, que está sob responsabilidade do Route 53. Ele faz o redirecionamento para o Amazon CloudFront, que é responsável por fazer a entrega de conteúdo com base na localização geográfica do usuário, na origem da página e também no servidor de entrega do conteúdo - realizando essa entrega com baixa latência e trazendo a sensação de “alta velocidade” por parte do usuário. O CloudFront está conectado com o Bucket S3, onde os arquivos do website estão armazenados. Todo esse acesso ao site é seguro e criptografado, através do certificado SSL gerado no Certificate Manager.</p>
<h3 id="ferramentas-e-serviços-utilizados">Ferramentas e serviços utilizados</h3>
<ul>
<li>Amazon Simple Storage Service (Amazon S3)</li>
<li>CloudFront</li>
<li>AWS Certificate Manager</li>
<li>Route 53</li>
</ul>
<h3 id="custos">Custos</h3>
<p>Os custos deste projeto vão depender se você pretende comprar um domínio ou hospedar um domínio já existente na AWS. Esses passos são opcionais, mas mesmo assim é válido elencar os preços.</p>
<ul>
<li><strong>Registro de domínio</strong>: para registros .br, o custo é R$ 40,00 caso você registre no <a href="https://registro.br/">Registro BR</a>. Para domínios com outras extensões, pode variar entre $3,00 a $5,00 (dólares), caso compre no <a href="https://www.namecheap.com">Namecheap</a> ou pela própria AWS.</li>
<li><strong>Utilizar a Zona Hospedada da AWS</strong>: $ 0.50 (dólares) por mês.</li>
</ul>

