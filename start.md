---
layout: default
css:
  - "/assets/plugins/prism/prism.css"
  - "/assets/plugins/elegant_font/css/style.css"
scripts:
  - "/assets/plugins/prism/prism.js"
  - "/assets/plugins/jquery-scrollTo/jquery.scrollTo.min.js"
bodyClass:
  - "body-green"
breadCrumbs: 
  - {active: "true", title: "Quick Start"}
---

<div id="doc-header" class="doc-header text-center">
    <h1 class="doc-title"><i class="icon fa fa-paper-plane"></i> Quick Start</h1>
    <div class="meta"><i class="fa fa-clock-o"></i> Last updated: Feb 17th, 2017</div>
</div><!--//doc-header-->
<div class="doc-body">
    <div class="doc-content">
        <div class="content-inner">
            <section id="installation-section" class="doc-section">
                <h2 class="section-title">Installation</h2>
                <div id="step1"  class="section-block">

                    <h3 class="block-title" id="step11">Composer</h3>
                    <p>You can install using <a href="http://getcomposer.org" target="_blank">composer</a>.</p>
                    <div class="code-block">
                        <h6>Latest release:</h6>
                        <p><code>composer require maiconpinto/cakephp-adminlte-theme</code></p>
                        <h6>Latest version (branch master):</h6>
                        <p><code>composer require maiconpinto/cakephp-adminlte-theme:dev-master</code></p>
                    </div><!--//code-block-->

                    <h3 class="block-title" id="step12">Enable Plugin</h3>
                    <div class="code-block">
                        <pre><code class="language-php">// config/bootstrap.php

Plugin::load('AdminLTE', ['bootstrap' => true, 'routes' => true]);</code></pre>
                    </div><!--//code-block-->

                    <h3 class="block-title" id="step13">Enable Theme</h3>
                    <div class="code-block">
                        <pre><code class="language-php">// src/Controller/AppController.php

public function beforeRender(Event $event)
{
    $this->viewBuilder()->theme('AdminLTE');
}</code></pre>
                    </div><!--//code-block-->


                    <h3 class="block-title" id="step14">Enable Form</h3>
                    <div class="code-block">
                        <pre><code class="language-php">// src/View/AppView.php

public function initialize()
{
    $this->loadHelper('Form', ['className' => 'AdminLTE.Form']);
}</code></pre>
                    </div><!--//code-block-->


                    <h3 class="block-title" id="step15">Configure</h3>
                    <div class="code-block">
                        <pre><code class="language-php">// src/Controller/AppController.php

use Cake\Core\Configure;

public function beforeRender(Event $event)
{
    // ...
    $this->set('theme', Configure::read('Theme'));
}</code></pre>
                        <pre><code class="language-php">// To customize configuration paste it at end of file config/bootstrap.php

Configure::write('Theme', [
    'title' => 'AdminLTE',
    'logo' => [
        'mini' => '<b>A</b>LT',
        'large' => '<b>Admin</b>LTE'
    ],
    'login' => [
        'show_remember' => true,
        'show_register' => true,
        'show_social' => true
    ],
    'folder' => ROOT,
    'skin' => 'blue'
    
]);

# skin options: 

# blue (Default)
# blue-light
# yellow
# yellow-light
# green
# green-light
# purple
# purple-light
# red
# red-light
# black
# black-light

</code></pre>
                    </div><!--//code-block-->




                    </div><!--//section-block-->
                    </section><!--//doc-section-->

                    </div><!--//content-inner-->
                    </div><!--//doc-content-->

                    <div class="doc-sidebar hidden-xs">
                        <nav id="doc-nav">
                            <ul id="doc-menu" class="nav doc-menu" data-spy="affix">
                                <li><a class="scrollto" href="#download-section">Download</a></li>
                                <li>
                                    <a class="scrollto" href="#installation-section">Installation</a>
                                    <ul class="nav doc-sub-menu">
                                        <li><a class="scrollto" href="#step11">Composer</a></li>
                                        <li><a class="scrollto" href="#step12">Enable Plugin</a></li>
                                        <li><a class="scrollto" href="#step13">Enable Theme</a></li>
                                        <li><a class="scrollto" href="#step14">Enable FormHelper</a></li>
                                        <li><a class="scrollto" href="#step15">Configure</a></li>
                                    </ul><!--//nav-->
                                </li>
                            </ul><!--//doc-menu-->
                        </nav>
                    </div><!--//doc-sidebar-->
                </div><!--//doc-body-->