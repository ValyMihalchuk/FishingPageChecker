**Краткое описание проекта**
- Название: "FishingPageChecker"
- В команде Виктор Ушков и Валентин Михальчук
- Безопасность пользователей в интернете -- актуальная проблема. Один из самых популярных методов взлома --  рассылка фишинговых писем. Решением проблемы могло бы служить браузерное расширение, предупреждающее пользователя о том, что он зашел фишинговый сайт
- Детектирование сайта происходит при помощи модели, полученной методом машинного обучения (метода random forest, возможно, будет применяться K-Nearest Neighbour или ANN)

**Предполагаемый сценарий использования**
Пользователь устанавливает в свой браузер расширение. При заходе пользователем на сайт, предпололожительно являющимся фишинговым, расширение показывает пользователю предупреждение об этом (и возможно главные критерии, по которым сайт показался расширению мошенническим - зависит от метода машинного обучения).

**Методы  машинного обучения, из которых мы будем выбирать наиболее подходящий для нашей задачи**
- *Random Forest*
Метод случайного леса — алгоритм машинного обучения, заключающийся в использовании ансамбля решающих деревьев.
- *K-Nearest Neighbour*
Метод ближайших соседей —  алгоритм для автоматической классификации объектов. В случае использования метода для классификации объект присваивается тому классу, который является наиболее распространённым среди соседей данного элемента, классы которых уже известны.
Простой в реализации, не самый простой в вычислении (если признаков слишком много).
- *ANN*

**Датасет для обучения**
Для обучения модели подходит [Phishing Website Dataset](https://archive.ics.uci.edu/dataset/327/phishing+websites). Этот датасет был собран из PhishTank archive, MillerSmiles archive, Google searching operators.
Вместе с датасетом там также приведены и подробно описаны признаки. Вот описание нескольких для примера:
- Using the IP Address
If an IP address is used as an alternative of the domain name in the URL, such as “http://125.98.3.123/fake.html”, users can be sure that someone is trying to steal their personal information. Sometimes, the IP address is even transformed into hexadecimal code as shown in the following link “http://0x58.0xCC.0xCA.0x62/2/paypal.ca/index.html”. 
- Long URL to Hide the Suspicious Part
Phishers can use long URL to hide the doubtful part in the address bar. For example: 
http://federmacedoadv.com.br/3f/aze/ab51e2e319e51502f416dbe46b773a5e/?cmd=_home&amp;dispatch=11004d58f5b74f8dc1e7c2e8dd4105e811004d58f5b74f8dc1e7c2e8dd4105e8@phishing.website.html
- Age of Domain
This feature can be extracted from WHOIS database (Whois 2005). Most phishing websites live for a short period of time. By reviewing our dataset, we find that the minimum age of the legitimate domain is 6 months. 


