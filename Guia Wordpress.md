<h1 id="guia-para-manutenção-e-modificação-de-plugins-wordpress">Guia para manutenção e modificação de plugins Wordpress</h1>
<p>Guia feito para auxiliar programadores de primeira viagem em manutenção ou modificação de plugins para Wordpress.</p>
<h2 id="primeiros-passos">Primeiros passos</h2>
<p>O passo inicial para conseguir entender bem plugins de terceiros é entendendo as convenções estabelecidas pela comunidade Wordpress e lendo a documentação da mesma para aprender o uso das funções mais usadas. A literatura presente nos links é de suma importância para melhor entendimento do guia, já que utilizarei termos que são explicados no mesmo e não me delongarei aqui os explicando.</p>
<h3 id="links-úteis">Links úteis:</h3>
<ul>
	<li><a href="https://docs.woocommerce.com/document/create-a-plugin/">Documentação do Wordpress para desenvolvimento de plugins</a></li>
	<li><a href="https://www.sitepoint.com/an-introduction-to-wordpress-plugin-development/">Guia introdutório para desenvolvimento de plugins</a></li>
	<li><a href="https://www.youtube.com/playlist?list=PLriKzYyLb28kR_CPMz8uierDWC2y3znI2">Curso em vídeo para desenvolvimento de plugins</a></li>
</ul>
<h2 id="estrutura-dos-arquivos">Estrutura dos arquivos</h2>
<p>O desenvolvimento de plugins para Wordpress não possui nenhuma framework oficial, assim nem tudo que está descrito aqui se encaixa em todos os plugins já que todos são desenvolvidos pela própria comunidade e nem todos dela possuem ciência dessas convenções não mandatórias seguidas pela comunidade.<br>
De acordo com a documentação, todo plugin DEVE ter um arquivo na raiz do diretório com o mesmo nome o diretório. Por exemplo, o nome do diretório é ‘syscoin-plugin’, assim, existe um arquivo nomeado ‘syscoin-plugin.php’, nele ocorre todo o core do plugin, na realidade, é possível plugins com apenas este arquivo, porém por motivos de manutenibilidade e modulação do código, você encontrará uma pasta de includes com outros arquivos, cada um responsável por uma área do plugin. É importante salientar que o Wordpress desencoraja objetos faz-tudo, assim, plugins sem essa estrutura de includes ou algo similar provavelmente recorrem a esta técnica, tornando mais difícil a manutenção do código. Junto com a pasta includes, é costume a internacionalização do plugin, assim, a pasta i18n é destinada para este fim.<br>
Por fim, outro fator importante para entender plugins é que são Orientados a Objetos, então a abordagem de definição de classes e a comunicação entre classes via construção de Objetos é bem comum e ajudam na modulação do código.</p>
<h2 id="workflow">Workflow</h2>
<p>A modificação de um plugin costuma ter 3 fases, estudo e entendimento do código, entender aonde as modificações devem ser feitas e identificar hooks mapeados para isso e implementar as modificações, testando a modificação com WP_DEBUG e, se possível, testes unitários.</p>
<h3 id="fase-1">Fase 1</h3>
<p>A primeira fase não tem muito erro ou dicas, é simplesmente, ler o código e entendê-lo usando os métodos que mais te traga resultados, deixei um link abaixo com algumas técnicas úteis para isso.</p>
<h3 id="fase-2">Fase 2</h3>
<p>Na fase dois, seu melhor amigo será o Google e a documentação do Wordpress e do Woocommerce, principalmente a documentação de hooks. Nela você decidirá onde serão suas modificações, se modificará alguma função já existente, ou se irá cadastrar novas funções a hooks escolhidos lendo as documentações. Um outro link que deixarei abaixo é uma referência visual dos hooks em páginas específica do Woocommerce, não é um material presente para todas as páginas do Wordpress e do Woocommerce, porém nas que possuem, é um atalho bem-vindo, por isso, recomendo sempre procurar esse tipo de material quando for procurar por hooks.</p>
<h3 id="fase-3">Fase 3</h3>
<p>Nesta fase é onde você colocará suas habilidades de programação em prática, é necessário um conhecimento ao menos básico da sintaxe do php e conhecer as funções mais comuns do Wordpress, muitas dessas funções você conhecerá nas Fases 1 e 2 já que vai se deparar com funções e métodos ainda não conhecidos e para cumprir bem essas fases será necessário entender boa parte dessa funções e métodos.</p>
<h3 id="links-úteis-1">Links Úteis:</h3>
<ul>
	<li><a href="https://make.wordpress.org/cli/handbook/plugin-unit-tests/">Testes unitários no Wordpress</a></li>
	<li><a href="https://selftaughtcoders.com/how-to-quickly-and-effectively-read-other-peoples-code/">Como ler códigos de outras pessoas</a></li>
	<li><a href="https://developer.wordpress.org/reference/hooks/">Lista de hooks do Wordpress</a></li>
	<li><a href="https://docs.woocommerce.com/wc-apidocs/hook-docs.html">Lista de hooks do Woocommerce</a></li>
	<li><a href="https://businessbloomer.com/woocommerce-visual-hook-guide-checkout-page/">Referência visual dos Hooks da página de Checkout do Woocommerce</a></li>
</ul>
<h2 id="considerações-finais">Considerações finais</h2>
<p>Não desanime com sua primeira tarefa de modificação ou manutenção de plugin! É um trabalho que demanda tempo e muita leitura de documentação e código para começar a pegar o jeito, a curva de aprendizado é íngrime, então será uma constante trilha adquirindo conhecimento.</p>

