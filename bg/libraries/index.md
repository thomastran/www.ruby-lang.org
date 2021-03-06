---
layout: page
title: "Библиотеки"
lang: bg
---

{% include out-of-date.html %}

Съществуват множество разнообразни библиотеки за Ruby, повечето от които
са под формата на *gem* пакети. Нека прегледаме някои от тях:
{: .summary}

### Намиране на библиотеки

[**RubyForge**][1] е известно място за Ruby библиотеки. Можете да
започнете със [софтуерната карта][2], която показва списък с достъпните
библиотеки, организирани по тема. (ако сте написали библиотека можете да
регистрирате вашия проект в Rubyforge, за да получите
свободен достъп до Subversion хранилище, хостинг и пощенски списъци.)

[**Ruby Application Archive**][3] (или RAA) е софтуерна директория за
библиотеки, организирана по функционалност.

### Използване на RubyGems

Ако сте използвали инсталатора на Ruby в Windows, вече разполагате с
RubyGems. За другите операционни системи това може да не е така –
прочетете [Инсталиране на RubyGems](#installing-rubygems).

#### Търсене на Gems

Командата **search** се използва за търсене на конкретна библиотека.
Следва пример с думата „html“ в името на библиотека:

{% highlight sh %}
$ gem search html --remote

*** REMOTE GEMS ***

html-sample (1.0, 1.1)
{% endhighlight %}

(*Флагът `--remote` / `-r` показва, че извършваме търсенето в Rubyforge.*)

#### Инсталиране на Gem

След като вече знаем името на библиотеката, следва и неговата
**инсталация**\:

{% highlight sh %}
$ gem install html-sample
{% endhighlight %}

Възможна е инсталация на определена версия на пакета. Ползва се
`--version` флага.

{% highlight sh %}
$ gem install html-sample --version 1.0
{% endhighlight %}

#### Извеждане на списък с достъпните за инсталация библиотеки:

За извеждането на пълен списък на достъпните библиотеки в Rubyforge,
ползваме следната команда:

{% highlight sh %}
$ gem list --remote
{% endhighlight %}

За да видите само инсталираните библиотеки, просто трябва да премахнете
флага `--remote`\:

{% highlight sh %}
$ gem list
{% endhighlight %}

За повече информация относно RubyGems, вижте [**официалното
ръководство**][4], което включва примери.

### Инсталиране на RubyGems
{: #installing-rubygems}

Инсталацията на RubyGems е елементарна. Свалете RubyGems от
[сайта][5]. Разархивирайте пакета и стартирайте `setup.rb`. На някои ОС
се изисква да имате администраторски права.

Пример за инсталация в Linux:

{% highlight sh %}
$ tar xzvf rubygems-0.9.*.tar.gz
$ cd rubygems-0.9.*
$ su -
$ ruby setup.rb
{% endhighlight %}

Ако имате нужда от информация за инсталирането на Ruby, моля посетете
[**секцията за инсталация**][6] в ръководството на RubyGems.



[1]: http://rubyforge.org/
[2]: http://rubyforge.org/softwaremap/trove_list.php
[3]: http://raa.ruby-lang.org/
[4]: http://rubygems.org/read/chapter/1
[5]: http://rubyforge.org/frs/?group_id=126
[6]: http://rubygems.org/read/chapter/3
