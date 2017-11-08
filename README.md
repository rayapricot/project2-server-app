# テクノロジー（藤原）第2回Webアプリ制作課題

## サンプル課題(Ruby): Nokogiriを用いて表を抜き出す

課題の詳細: [第2回 サーバサイドスクリプトの制作 - テクノロジー（藤原）2017年度資料](https://kd-site2017.firebaseapp.com/project2-server-app/)

## 以下、自分で記入してください。（レポートの代わりとします）

`（ここに貼り付ける）` や `（ここに書く）` の部分を自分で削除して、そこに自分で記入してください。

----------------------

## 実行コマンドと結果

Cloud9のBash(端末)で`ruby`コマンドを実行し、そのコマンドと結果をコピーして貼り付けてください。

- 課題の要件（表を抜き出す）が満たされているかどうかのチェックです
- 他のコマンド(`git`, `bundle`, `ls`など)は不要です

```
 (master) $ bundle install
Using bundler 1.15.4
Using byebug 9.1.0
Using coderay 1.1.2
Using method_source 0.9.0
Using mini_portile2 2.3.0
Using pry 0.11.2
Using nokogiri 1.8.1
Using pry-byebug 3.5.0
Bundle complete! 3 Gemfile dependencies, 8 gems now installed.
Use `bundle info [gemname]` to see where a bundled gem is installed.
rayapricot:~/workspace/project2-server-app (master) $ ruby get_table.rb
Introduction
Choosing
Current Releases/Repositories
Production Releases
Release statistics
Workflow
Codenames
See also
rayapricot:~/workspace/project2-server-app (master) $ doc
bash: doc: command not found
rayapricot:~/workspace/project2-server-app (master) $ doc
bash: doc: command not found
rayapricot:~/workspace/project2-server-app (master) $ ruby get_table.rb

From: /home/ubuntu/workspace/project2-server-app/get_table.rb @ line 13 :

     8: 
     9: # 下の行をコメントアウトすると、pryが起動する
    10:  binding.pry
    11: 
    12: # 例：h2要素のみを抜き出す
 => 13: doc.css('h2').each do |node|
    14:   puts node.text
    15: end

[1] pry(main)> doc
=> #(Document:0x1462ebc {
  name = "document",
  children = [
    #(DTD:0x157cc44 {
      name = "HTML"
      }),
    #(Element:0x1582ea0 {
      name = "html",
      children = [
        #(Text "\n"),
        #(Element:0x158d698 {
          name = "head",
          children = [
            #(Text "\n"),
[2] pry(main)> doc.class
=> Nokogiri::HTML::Document
[3] pry(main)> node.class
NameError: undefined local variable or method `node' for main:Object
from (pry):3:in `<main>'
[4] pry(main)> node.text
NameError: undefined local variable or method `node' for main:Object
from (pry):4:in `<main>'
[5] pry(main)> doc
=> #(Document:0x1462ebc {
  name = "document",
  children = [
[7] pry(main)> 
[8] pry(main)> 
[9] pry(main)> 
[10] pry(main)> 
[11] pry(main)> 
[12] pry(main)> 0 times {|i| print i, ", "}
[13] pry(main)> 
[14] pry(main)>  = ["りんご","みかん","ぶ ど
[15] pry(main)> 
[16] pry(main)> 
[17] pry(main)> 
[18] pry(main)> 
[19] pry(main)> 
[20] pry(main)> 
[21] pry(main)> 
[22] pry(main)> 
[23] pry(main)> 
[24] pry(main)> 
[25] pry(main)> 
[26] pry(main)> 
[27] pry(main)> ruby get_table.rb
NameError: undefined local variable or method `get_table' for main:Object
from (pry):7:in `<main>'
[28] pry(main)> 下t
NameError: undefined local variable or method `下t' for main:Object
from (pry):8:in `<main>'
[29] pry(main)> get_table.rb
NameError: undefined local variable or method `get_table' for main:Object
from (pry):9:in `<main>'
[30] pry(main)> exit
Introduction
Choosing
Current Releases/Repositories
Production Releases
Release statistics
Workflow
Codenames
See also
rayapricot:~/workspace/project2-server-app (master) $ ruby get_table.rb

From: /home/ubuntu/workspace/project2-server-app/get_table.rb @ line 13 :

     8: 
     9: # 下の行をコメントアウトすると、pryが起動する
    10:  binding.pry
    11: 
    12: # 例：h2要素のみを抜き出す
 => 13: doc.css('table').each do |node|
    14:   puts node.text
    15: end

[1] pry(main)> exit
   Version 
   Code name 
   Release date 
   End of life date 

   
   Bullseye 
   
   

   
   Buster 
   
   

   9 
   Stretch 
   June 17th 2017 
   approx. 2020 (full) / approx. 2022 (LTS)  

   8 
   Jessie   
   April 25th 2015    
   ~June 6th 2018 (full) / ~June 6th 2020 (LTS) 

   7 
   Wheezy   
   May 4th 2013       
   April 26th 2016 (full) / May 2018 (LTS) 

   6.0 
   Squeeze 
   February 6th 2011 
   May 31st 2014 (full) / February 29th 2016 (LTS) 

   5.0 
   Lenny     
   February 14th 2009 
   February 6th 2012 

   4.0 
   Etch       
   Apr 8th 2007       
   February 15th 2010 

   3.1 
   Sarge     
   June 6th 2005      
   March 31st 2008 

   3.0 
   Woody     
   July 19th 2002     
   June 30th 2006  

   2.2 
   Potato   
   August 15th 2000   
   June 30th 2003 

   2.1 
   Slink     
   March 9th 1999     
   September 30th 2000 (full) / October 30th 2000 (limited) 

   2.0 
   Hamm       
   July 24th 1998     
   - 

   1.3 
   Bo           
   July 2nd 1997      
   - 

   1.2 
   Rex         
   December 12th 1996 
   - 

   1.1 
   Buzz       
   June 17th 1996     
   - 

   0.93R6 
                          
   October 26 1995    
   - 

   0.93R5 
                          
   March 1995         
   - 

   0.91   
                          
   January 1994 
   - 

    Version 
   Code name 
   Freeze length 
   Time from previous release 
   Time from next release up to EOL 
   Total lifetime 

   1.2 
   Rex 
   
   178 days 

   1.3 
   Bo 
   
   175 days 

   2.0 
   Hamm 
   171 days 
   414 days 

   2.1 
   Slink 
   125 days 
   228 days 
   76 days 
   601 days 

   2.2 
   Potato 
   212 days 
   525 days 
   346 days 
   1049 days 

   3.0 
   Woody 
   383 days 
   703 days 
   389 days 
   1442 days 

   3.1 
   Sarge 
   34 days 
   1053 days 
   357 days 
   1028 days 

   4.0 
   Etch 
   258 days 
   671 days 
   366 days 
   1044 days 

   5.0 
   Lenny
   202 days 
   678 days 
   365 days 
   1087 days 

   6.0 
   Squeeze 
   184 days 
   722 days 
   391 days 

   7.0 
   Wheezy 
   818 days 
   367 days 

   8.0 
   Jessie 
   171 days 
   721 days 

   9.0 
   Stretch 
   224 days 
   784 days 

rayapricot:~/workspace/project2-server-apprayapricot:~/workspace/project2-server-app (master) $ 
rayapricot:~/workspace/project2-server-app (master) $ git add *
rayapricot:~/workspace/project2-server-app (master) $ git commit -m '10/25 授業'
[master 93530ae] 10/25 授業
 1 file changed, 2 insertions(+), 2 deletions(-)
rayapricot:~/workspace/project2-server-app (master) $ git push
Warning: Permanently added 'github.com,192.30.253.113' (RSA) to the list of known hosts.
Counting objects: 3, done.
Delta compression using up to 8 threads.
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 308 bytes | 308.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To github.com:rayapricot/project2-server-app.git
   09e5009..93530ae  master -> master
rayapricot:~/workspace/project2-server-app (master) $ git add *
rayapricot:~/workspace/project2-server-app (master) $ 
rayapricot:~/workspace/project2-server-app (master) $ git commit -m '11/1 授業'
On branch master
Your branch is up-to-date with 'origin/master'.

nothing to commit, working tree clean
rayapricot:~/workspace/project2-server-app (master) $ git push
Warning: Permanently added 'github.com,192.30.253.113' (RSA) to the list of known hosts.
Everything up-to-date
rayapricot:~/workspace/project2-server-app (master) $ 
```

## Rubyや課題に関して、難しかったこと・分からなかったこと



## Rubyを触ってみた・課題をやってみた感想

Rubyを初めて触ったのですが，初心者の自分でも書きやすいと感じました．

