## Laravel-4.2-with-Bootstrap
Laravel-4.2 with Bootstrap is a package which can be used as a starter point.

## Purpose
It will make easier for developer who want to use Bootstrap as their front end tool.
It is a package of Laravel-4.2-with-Bootstrap-3.3.1.

## Installation
<ul>
<li><a href="#install-composer">Install Composer</a></li>
<li><a href="#install-laravel">Install Laravel</a></li>
<li><a href="#server-requirements">Server Requirements</a></li>
<li><a href="#configuration">Configuration</a></li>
<li><a href="#pretty-urls">Pretty URLs</a></li>
</ul>


<p><a name="install-composer"></a></p>
<h2>1. Install Composer</h2>
<p>Laravel utilizes <a href="http://getcomposer.org">Composer</a> to manage its dependencies. First, download a copy of the <code>composer.phar</code>. Once you have the PHAR archive, you can either keep it in your local project directory or move to <code>usr/local/bin</code> to use it globally on your system. On Windows, you can use the Composer <a href="https://getcomposer.org/Composer-Setup.exe">Windows installer</a>.</p>



<h2>2. Install Laravel</h2>

<h3>
<a id="user-content-step-1-get-the-code" class="anchor" href="#step-1-get-the-code" aria-hidden="true"><span class="octicon octicon-link"></span></a>Step 1: Get the code</h3>

<h4>
<a id="user-content-option-1-git-clone" class="anchor" href="#option-1-git-clone" aria-hidden="true"><span class="octicon octicon-link"></span></a>Option 1: Git Clone</h4>

<div class="highlight highlight-bash"><pre>$ git clone https://github.com/saidurcse/Laravel-4.2-with-Bootstrap.git</pre></div>

<h4>
<a id="user-content-option-2-download-the-repository" class="anchor" href="#option-2-download-the-repository" aria-hidden="true"><span class="octicon octicon-link"></span></a>Option 2: Download the repository</h4>

<pre><code>https://github.com/saidurcse/Laravel-4.2-with-Bootstrap-master.zip
</code></pre>

<h3>
<a id="user-content-step-2-use-composer-to-install-dependencies" class="anchor" href="#step-2-use-composer-to-install-dependencies" aria-hidden="true"><span class="octicon octicon-link"></span></a>Step 2: Use Composer to install dependencies</h3>

<h4>
<a id="user-content-option-1-composer-is-not-installed-globally" class="anchor" href="#option-1-composer-is-not-installed-globally" aria-hidden="true"><span class="octicon octicon-link"></span></a>Option 1: Through Composer command we can resolve the dependencies</h4>

<div class="highlight highlight-bash"><pre>$ <span class="pl-s3">cd</span> laravel
$ composer update</pre></div>

<h3>
<a id="user-content-step-1-get-the-code" class="anchor" href="#step-1-get-the-code" aria-hidden="true"><span class="octicon octicon-link"></span></a>Step 3: Configure Database</h3>
<h4>Option 1: Configure the following file <pre>app/config/database.php</pre></h4>




<p><a name="server-requirements"></a></p>
<h2>3. Server Requirements</h2>
<p>The Laravel framework has a few system requirements:</p>
<ul>
<li>PHP >= 5.4</li>
<li>MCrypt PHP Extension</li>
</ul>
<p>As of PHP 5.5, some OS distributions may require you to manually install the PHP JSON extension. When using Ubuntu, this can be done via <code>apt-get install php5-json</code>.</p>
<p><a name="configuration"></a></p>


<p><a name="configuration"></a></p>
<h2>4. Configuration</h2>
<p>Laravel needs almost no configuration out of the box. You are free to get started developing! However, you may wish to review the <code>app/config/app.php</code> file and its documentation. It contains several options such as <code>timezone</code> and <code>locale</code> that you may wish to change according to your application.</p>
<p>Once Laravel is installed, you should also <a href="/docs/configuration#environment-configuration">configure your local environment</a>. This will allow you to receive detailed error messages when developing on your local machine. By default, detailed error reporting is disabled in your production configuration file.</p>
<blockquote>
<p><strong>Note:</strong> You should never have <code>app.debug</code> set to <code>true</code> for a production application. Never, ever do it.</p>
</blockquote>
<p><a name="permissions"></a></p>
<h3>Permissions</h3>
<p>Laravel may require one set of permissions to be configured: folders within <code>app/storage</code> require write access by the web server.</p>
<p><a name="paths"></a></p>
<h3>Paths</h3>
<p>Several of the framework directory paths are configurable. To change the location of these directories, check out the <code>bootstrap/paths.php</code> file.</p>




<p><a name="pretty-urls"></a></p>
<h2>5. Pretty URLs</h2>
<h3>Apache</h3>
<p>The framework ships with a <code>public/.htaccess</code> file that is used to allow URLs without <code>index.php</code>. If you use Apache to serve your Laravel application, be sure to enable the <code>mod_rewrite</code> module.</p>
<p>If the <code>.htaccess</code> file that ships with Laravel does not work with your Apache installation, try this one:</p>
<pre><code>Options +FollowSymLinks
RewriteEngine On

RewriteCond %{REQUEST_FILENAME} !-d
RewriteCond %{REQUEST_FILENAME} !-f
RewriteRule ^ index.php [L]</code></pre>
<h3>Nginx</h3>
<p>On Nginx, the following directive in your site configuration will allow "pretty" URLs:</p>
<pre><code>location / {
    try_files $uri $uri/ /index.php?$query_string;
}</code></pre>
            



## DOCUMENTATION
http://laravel.com/docs/4.2/configuration

## License

The Laravel framework is open-sourced software licensed under the [MIT license](http://opensource.org/licenses/MIT)
