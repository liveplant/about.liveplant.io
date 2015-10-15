# about.liveplant.io

This repo serves two purposes: 

1. Central place for documenting decision making regarding the liveplant.io
   project
2. Explaining liveplant to external users

This site is built with [Jekyll][]. I recommend you visit [the Jekyll docs][]
and take a look at the [GitHub Pages instructions][].

## Dependencies

<table class="table">
  <caption></caption>
  <thead>
    <tr>
      <th>Dependency</th>
      <th>Install Options <br> (Linux, Unix, Mac OS X)</th>
      <th>Install Options <br> (Windows)</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Ruby</td>
      <td>
        <ul>
          <li><strong>Recommended:</strong> Use <a href="https://rvm.io">RVM</a></li>
          <li>Ruby comes with your Mac and most *nix distros</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>Use <a href="http://rubyinstaller.org/">RubyInstaller</a></li>
        </ul>
      </td>
    </tr>
    <tr>
      <td>Bundler</td>
      <td><code>gem install bundler</code></td>
      <td><code>gem install bundler</code></td>
    </tr>
    <tr>
      <td>
        Python
        (required by Jekyll)
      </td>
      <td>
        <ul>
          <li>Python comes with your Mac and most *nix distros</li>
        </ul>
      </td>
      <td>
        <ul>
          <li>Download <a href="https://www.python.org/ftp/python/2.7.10/python-2.7.10.msi">here</a> (version 2.7.10).</li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

## Get Started

1. Clone this repo
```
git clone git@github.com:liveplant/about.liveplant.io.git
```
2. Install project dependencies
```
bundle install
```
3. Run jekyll
```
bundle exec jekyll serve
```
4. You should have a site running at http://0.0.0.0:4000/ (or http://127.0.0.1:4000/)

[Jekyll]: http://jekyllrb.com/
[the Jekyll docs]: http://jekyllrb.com/docs/home/
[GitHub Pages instructions]: https://help.github.com/articles/using-jekyll-with-pages/
