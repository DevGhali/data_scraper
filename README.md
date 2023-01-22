data_scraper
</br>
simple stupid script in python that scrapes data from a website, looks for certain urls inside the html code based on a suffix string given. (explanation below)

* TL;DR what does it do exactly??
</br>
this script dives into the html code of a website given using basic GET requests and based on a suffix provided (e.g a string ".png"/".jpg") searches inside the html code for more urls that end with the suffix, then it writes to the disk on a provided directory the files from the urls it has found.

</br>
Didnt unsterstand anyhting pls give an example!!

for this example lets say we want to get all ".jpg" files from a website.

1. fill the information needed such as :

- Website   we want to get the data from (url - "https://www.xyz.xyz")
- suffix    (suffix - ".jpg")
- directory (dir - /Users/user/Desktop/)
- file name (file_name - "what you want the files to be called") as for the files names, it will use the given file_name + a number at the beginning in an             scending order.  e.g  file_name = "abc", the files will be called as follows "0abc", "1abc", "2abc" and so on.
-headers    (headers - here you can provide your User-Agent or different headers and params for the GET requests)

2. after running the script it will make a GET request and store the raw html code, using 're' it will find, filter and store all urls from the raw code in a list.

3. using the sanitize function it will sanitize and keep only the urls that end with the suffix given (".jpg").

4. and last of all, after it has created a list that contains urls to jpgs it will start writing the files to the disk.

