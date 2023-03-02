extra steps to fix my issues
```
ruby -e 'require "jekyll-import";
JekyllImport::Importers::WordpressDotCom.run({
  "source" => "/home/jr/Documents/blog.betterdevthanyesterday/betterdevthanyesterday.WordPress.2023-02-24.xml",
  "no_fetch_images" => false,
  "assets_folder" => "assets/images"
})'
```
```
ruby -rubygems -e 'require "jekyll-import";
JekyllImport::Importers::WordpressDotCom.run({
  "source" => "<path-to-XML-export>",
  "no_fetch_images" => false,
  "assets_folder" => "assets/images"
})'
```
sed -i.bak 's/https:\/\/blog.josedromero.com//g' *.md
```
