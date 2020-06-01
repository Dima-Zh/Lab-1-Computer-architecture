# Lab-1-Computer-architecture

Виконали студенти КВ-73 
Шаган Сергій та Жовнірський Дмитро

                                                           Варіант 5
"ПЗ для створення плейлистів. Реалізувати проходження по сторінкам з набору url, які задані у вхідному xml-файлі, а також по сторінкам, на які є посилання з цих сторінок з заданою глибиною вкладеності. На всіх цих сторінках знайти всі посилання на mp3-файли, знайдені файли відфільтрувати за заданим жанром, який зберігається у ID3-запису, та результат зберігти у файл в форматі xml. "


Для того щобзапустити ПЗ необхідно використовувати із site_parser/site_parser.py 
ось цей scrape_mp3_from_sites

Виклику ПЗ:
```
from site_parser import site_parser
site_parser.scrape_mp3_from_sites("data.xml",1)
```
data.xml - вхідний файл з сайтами для сканування  
1 - рівень заглиблення

Вхідний xml файл
```
<?xml version="1.0"?>
<data>
    <site>https://mp3-music.club/hity-2017/</site>
    <site>https://drivemusic.me/pop_music/35672-a-ha-lifelines.html</site>
</data>
```

Вихідний xml файл
```
<?xml version="1.0" ?>
<Playlist>
	<Genre name="genre1">
		<music>
			<filename>music1.mp3</filename>
			<title>Music titel</title>
			<link>https://www.somesite.com/mp3/music1.mp3</link>
		</music>
		<music>
			<filename>music2.mp3</filename>
			<title>Music title2</title>
			<link>https://www.somesite.com/mp3/music2.mp3</link>
		</music>
  </Genre>
</Playlist>
```
