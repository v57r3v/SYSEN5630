java c
SYSEN5630
Assignment   1
Due:   5pm   EST, 2/08/2025


1.      Regular expression patterns
Write   regular   expressions   matching   the   following   patterns.   The   matching   should   cover   the   entire   input   string (not   partial).


1 import re
2
3 def isMatch(s, p):
4 """
5 :type s: str. Input string
6 :type p: str. Regular expression
7 :rtype: bool
8 """
9 print(’Input: s="%s", p="%s"’ % (s, p))
10 m = re.match(p, s, re.A)
11 r = m is not None and m.end() == len(s)
12 print(’Output: %s’ % r)
1 >> isMatch("begn", "beg.n")
2 Input: s="begn", p="beg.n"
3 Output: False
4
5 >> isMatch("begin", "beg.n")
6 Input: s="begin", p="beg.n"
7 Output: True


(a)    Write   one   regular   expression   that   matches   DNA   (strings   of   A,C,G, or   T) in   upper/lower   case
Return   True:
•      acgtagaatgacatactgactgactactagcatgactgactgactg
•      catcatcatcatcatcatcatcatcatcatcatcat
•      ACtCtATCtCTAtcttAtaCtCTAtgTGCgGAGAggGag
•    catcatcatcatmeowcatcatmeow




Return False:

•      tagtagtagtagbodyspraytagtagtagtag
•      actg   actga   actga   tacgtagtc   tag   atcg   actgac   tg   a
•      12345
(b)    Write   one   regular   expression   that   matches   words   containing   at   least   two   vowels   (a,   e,   i,   o, u,   A,   E,   I,   O,   or   U).
Return   True:
•    Jamie
•    Michael
•      Staci
•      David
•    Phillip
•      either
Return False:
•      Shiny
•    Zack
•      Katlyn
•    Chris
(c)    Write   one   regular   expression   that   matches   dollar   amounts   of   at   least   $1000.00.   
Return   True:

•      $1000.01
•      $1234.12
•    $1221222121212.00
Return False:
•      1000.00
•      $010.00
•      $499.99
•      $1000.121


2.      Regular expression for sentence split
The      chemprot         sample         abstracts-10   .tsv   file   contains   plain-text,   UTF8-encoded   CHEMPROT   sample set PubMed record in a tab-separat代 写SYSEN5630 Assignment 1Python
代做程序编程语言ed format with the following   three   columns:
•    Article   identifier   (PMID, PubMed   identifier)
•    Title   of   the   article
•    Abstract   of   the   article
A   total   of   10 records   are   provided   in   this   sample   set.
(a)      Write a   Python script. and   use   [ˆ\   .   \!\?]   * [\   .   \!\?]   to   extract   sentences   from   each abstract. How   many   sentences   can   be   extracted   from   each   abstract   (NOT   the   title)?
PMID
Number   of   sentences   in   the   abstract   (3rd   column)
Example:   10471277
11
23150485
   
23155202
   
23477624
   
23044094
   
23220749
   
9950599
   
23615073
   
23147415
   
23643664
   
(b)    Give   2 examples   that   the   extracted   text   is   not   a   complete   sentence   and   explain   why   the   regular   expres-   sion   does   not   work.
(c)    Submit   the   runnable   script.
3.    Text   preprocessing
The chemprot         sample         abstracts   .tsv   file contains   plain-text, UTF8-encoded CHEMPROT sample   set PubMed record in a tab-separated format with the following three columns:
•    Article   identifier   (PMID, PubMed   identifier)
•    Title   of   the   article
•    Abstract   of   the   article
In   total   50 records   are   provided   in   this   sample   set, where   each   line   contains   a   single   PMID, title, and   abstract separated by tabulators.
(a)    Calculate   the   total   number   of   sentences,   the   number   of   unique   words,   and   the   number   of   unique   lemmas in all   abstracts.
   
NLTK
Spacy
Stanza
Sentences
   
   
   
Unique Words
   
   
   
Unique Lemmas
   
   
   
(b)    Upload   the   source   codes.
(c)    Find   2 tokenization   examples   in   the   dataset   that   Spacy   and   Stanza   return   differently.
(d)    Find   2 lemmatization   examples   in   the   dataset   that   Spacy   and   Stanza   return   differently.

         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
