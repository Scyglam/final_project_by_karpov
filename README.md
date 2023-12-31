# final_project

Стек: Pandas, seaborn, matplotlib, numpy, scipy.stats, bootstrap, A/B тест.

Основные цели: 

Мы работаем в компании, разрабатывающей мобильные игры.

1) Написать функцию для подсчета метрики retention (по дням от даты регистрации игрока).

2) Имеются результаты A/B теста, в котором двум группам пользователей предлагались различные наборы акционных предложений. Известно, что ARPU в тестовой группе выше на 5%, чем в контрольной. При этом в контрольной группе 1928 игроков из 202103 оказались платящими, а в тестовой – 1805 из 202667. На основе имеющихся данных определить, какой набор можно считать лучшим и на основе каких метрик стоит принять правильное решение.

3) В игре Plants & Gardens каждый месяц проводятся тематические события, ограниченные по времени. В них игроки могут получить уникальные предметы для сада и персонажей, дополнительные монеты или бонусы. Для получения награды требуется пройти ряд уровней за определенное время. С помощью каких метрик можно оценить результаты последнего прошедшего события?

Предположим, в другом событии мы усложнили механику событий так, что при каждой неудачной попытке выполнения уровня игрок будет откатываться на несколько уровней назад. Изменится ли набор метрик оценки результата? Если да, то как?.

Полученные результаты: 

1) Показатель retention растет линейно достигая своего пика на 5-7 день после регистрации. То есть пользователи доходят до пика интереса, а затем наблюдается постепенный спад. Это может быть вызвано проблемами как с техническими аспектами игры, так и с гейплеем. Возможно стоит поработать с игровой механикой, ввести бонусы каждый день с внутриигровой валютой, улучшить сам код и оптимизацию, можно придумать различные внутриигровые ивенты завязанные на днях недели. Возможно стоит больше вложиться в таргетированную рекламу.

2) Если мы допускаем что дизайн эксперимента не был нарушен, то мы можем сделать следующие выводы: 

а) При сравнении всех пользователей, включая и платящих и не платящих, статистически значимых различий между группами не обнаружено. Это означает, что акционные предложения, предоставленные тестовой группе, не оказали статистически значимого влияния на общую аудиторию игроков.

б) Однако, если сравнить только платящих пользователей, выявляются статистически значимые различия между группами. Это говорит о том, что акционные предложения имеют положительный эффект на платящих пользователей и способствуют повышению ключевых метрик, связанных с доходом или активностью платежей.

в) Конверсия в покупку статистически значимо выше в контрольной группеНа основе этих результатов можно рекомендовать использовать набор акционных предложений, предоставленный тестовой группе, в дальнейшем. Он демонстрирует статистически значимое улучшение показателей среди платящих пользователей. Однако, следует учесть, что данная рекомендация основана на предположении, что выборка и методология анализа были надлежащими, и нет других факторов, которые могли повлиять на результаты.

3)  Для оценки результатов последнего прошедшего события в игре Plants & Gardens можно использовать следующие метрики:
Прохождение уровней: Оценка количества уровней, пройденных игроком за время события. Эта метрика позволяет определить, насколько успешно игроку удалось прогрессировать в событии и достичь поставленных целей.

Время завершения: Оценка времени, затраченного игроком на прохождение события. Быстрое завершение события может свидетельствовать о высоком уровне навыков и эффективной стратегии игрока.

Количество ошибок: Оценка количества ошибок, допущенных игроком во время прохождения уровней. Меньшее количество ошибок может указывать на лучшую игровую стратегию и навыки игрока.

Полученные награды: Оценка полученных игроком уникальных предметов для сада и персонажей, дополнительных монет или бонусов. Эта метрика позволяет измерить успешность игрока в том, что касается получения и использования наград, которые были доступны в рамках события.

Если в другом событии усложнена механика так, что при неудачной попытке выполнения уровня игрок будет откатываться на несколько уровней назад, набор метрик для оценки результатов может измениться. В таком случае можно добавить следующую метрику:

Количество откатов: Оценка количества откатов, сделанных игроком во время события. Эта метрика позволяет измерить сложность уровней и эффективность игрока в их преодолении. Меньшее количество откатов может указывать на более опытного игрока или лучшую адаптацию к измененной механике события.
Таким образом, в случае изменения механики событий с откатом уровней, метрики оценки результатов могут включать информацию о количестве откатов, чтобы более точно оценить успешность игрока в новых условиях игры.