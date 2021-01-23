# act1

```
SceneSetup.act1();
```

(...300)

n: И ЭТО ТРЕВОГА ЧЕЛОВЕКА

n: _ТЫ_ И ЕСТЬ ТРЕВОГА

{{if window.localStorage.continueChapter=="replay"}}
(#act1_replay)
{{/if}}

{{if window.localStorage.continueChapter!="replay"}}
(#act1_normal)
{{/if}}

# act1_replay

`hong({mouth:"0_neutral", eyes:"0_neutral"})`

h: Оу, хэй! Мы снова вернулись сюда?

`hong({eyes:"0_neutral"})`

n: ТВОЯ ЗАДАЧА - ЗАЩИЩАТЬ СВОЕГО ЧЕЛОВЕКА ОТ *ОПАСНОСТЕЙ*

`bb({eyes:"look", mouth:"small_lock"})`

n: ФАКТИЧЕСКИ, ПЕРЕПРОХОДЯ ЭТУ ИГРУ ОН ПОДВЕРГАЕТ СЕБЯ *ОПАСНОСТИ*

n: СКОРЕЕ, ПРЕДУПРЕДИ ЕГО!

```
sfx("squeak");
bb({body:"squeeze_talk"});
hong({body:"0_squeeze"});
```

b: Человек! Слушай, мы в опасности! Игрок...

[...собирается снова нас мучать!](#act1_replay_torture)

[...не может найти альтернативную концовку!](#act1_replay_alternate)

[...получит лудо-нарративный диссонанс!](#act1_replay_dissonance)

# act1_replay_torture

```
window.HACK_REPLAY = JSON.parse(localStorage.act4);
bb({body:"normal", mouth:"normal", eyes:"fear"});
hong({body:"0_sammich"});
```

{{if window.HACK_REPLAY.act1_ending=="fight"}}
b: Он заставит нас свернуться в клубок и плакать!
{{/if}}

{{if window.HACK_REPLAY.act1_ending=="flight"}}
b: Он заставит нас сломать твой телефон и вызвать паническую атаку!
{{/if}}

{{if window.HACK_REPLAY.a2_ending=="fight"}}
b: Он заставит нас *НЕ* бить хозяина вечеринки!
{{/if}}

{{if window.HACK_REPLAY.a2_ending=="flight"}}
b: Он заставит нас ударить симпатичного анти-злодейского хозяина вечеринки!
{{/if}}

{{if window.HACK_REPLAY.a3_ending=="jump"}}
h: Ну, по крайней мере, мы не спрыгнем с крыши в этот р--
{{/if}}

{{if window.HACK_REPLAY.a3_ending=="walkaway"}}
b: ОН ЗАСТАВИТ НАС СПРЫГНУТЬ С КРЫШИ.
{{/if}}

`bb({body:"fear"});`

b: ВСЕ ЭТИ УЖАСНЫЕ ВЕЩИ ПРОИЗОЙДУТ С НАМИ, И ТОГДА МЫ--

(#act1_replay_end)


#act1_replay_alternate

```
bb({body:"normal", mouth:"normal", eyes:"fear"});
hong({body:"0_sammich"});
```

h: Конечно, история *в целом* та же, но каждая глава имеет две возможные концовки, плюс все варианты других диалога--

`bb({body:"fear"});`

b: Игрок разочаруется, закроет эту вкладку браузера, удалит нашу программу, и тогда мы--

(#act1_replay_end)


# act1_replay_dissonance

```
bb({body:"normal", mouth:"normal", eyes:"fear"});
hong({body:"0_sammich"});
```

h: Да чёрт, что сейчас?

`bb({eyes:"normal"});`

b: Сюжет истории был о том, как ты можешь *ВЫБРАТЬ* построение хорошего сотрудничества со своим страхом,

`bb({eyes:"normal_right"});`

b: Но повторное прохождение игры даст ту же историю, подразумевая, что твой *ВЫБОР* не имеет значения,

`bb({eyes:"narrow_eyebrow"});`

b: Таким образом, показывая противоречие между связью игры и механикой,

`bb({eyes:"fear"});`

b: Таким образом, распутывая ткань этой повествовательной вселенной,

`bb({body:"fear"});`

b: И тогда мы--

(#act1_replay_end)


# act1_replay_end

`bb({body:"panic"})`

b: УМРЁЁЁЁЁЁЁЁЁЁЁЁЁЁЁЁЁМ

```
bb({body:"normal", mouth:"normal", eyes:"normal"});
Game.clearText();
```

(...1001)

```
bb({body:"laugh"});
hong({body:"laugh"});
Game.clearText();
sfx("laugh");
```

(...5001)

```
bb({body:"normal", mouth:"normal", eyes:"normal"});
hong({body:"0_sammich"});
```

h: Окей, давай вернёмся в роль.

```
Game.clearText();
```

n4: (ПОЗВОЛЬ _ТВОЕЙ_ ТРЕВОГЕ БЛА БЛА БЛА ЧТО ГОВОРИТ ТЕБЕ _ТВОЙ_ СТРАХ БЛА БЛА НУ КОРОЧЕ ТЫ ПОНЯЛ)

```
sfx("squeak");
hong({body:"0_squeeze"});
bb({body:"squeeze"});
```

(#act1_normal_choice)



# act1_normal

`hong({mouth:"0_neutral", eyes:"0_annoyed"})`

h: Ну класс, мой волк вернулся. Фааааантастика.

`hong({eyes:"0_neutral"})`

n: ТВОЯ ЗАДАЧА - ЗАЩИЩАТЬ СВОЕГО ЧЕЛОВЕКА ОТ *ОПАСНОСТЕЙ*

`bb({eyes:"look", mouth:"small_lock"})`

n: ФАКТИЧЕСКИ, ЭТОТ СЭНДВИЧ ПРЯМО СЕЙЧАС ПОДВЕРГАЕТ ЕГО *ОПАСНОСТИ*

n: СКОРЕЕ, ПРЕДУПРЕДИ ЕГО!

```
sfx("squeak");
bb({body:"squeeze_talk"});
hong({body:"0_squeeze"});
```

b: Человек! Слушай, мы в опасности! Опасность в том, что...

`bb({body:"squeeze"})`

n4: ПОЗВОЛЬ _ТВОЕЙ_ ТРЕВОГЕ СЫГРАТЬ! ВЫБЕРИ ТО, ЧТО ГОВОРИТ ТЕБЕ ГОВОРИТ _ТВОЙ_ СТРАХ

(#act1_normal_choice)

# act1_normal_choice

[Мы обедаем одни! Снова!](#act1a_alone) `bb({body:"squeeze_talk"})`

[Мы не продуктивны, пока едим!](#act1a_productive) `bb({body:"squeeze_talk"})`

[Этот белый хлеб плох для нас!](#act1a_bread) `bb({body:"squeeze_talk"})`

# act1a_alone

```
bb({body:"normal", mouth:"small", eyes:"narrow"});
hong({body:"0_sammich"});
```

b: Разве ты не знаешь, что одиночество приводит к преждевременной смерти - точно так же, как курение 15 сигарет в день?-

`Game.OVERRIDE_TEXT_SPEED = 2;`

`bb({mouth:"normal", eyes:"normal_right"})`

b: (Holt-Lunstad 2010, PLoS Medicine)

`hong({eyes:"0_annoyed"})`

h: Эм, спасибо за цитирование своих источников, но--

`Game.OVERRIDE_TEXT_SPEED = 2;`

`bb({body:"fear", mouth:"normal", eyes:"fear"})`

b: Это значит, что если мы не будем тусоваться с кем-нибудь *прямо сейчас*, то мы-

`bb({body:"panic"})`

b: УМРЁЁЁЁЁЁЁЁЁЁЁЁЁЁЁЁЁМ

```
bb({body:"normal", mouth:"normal", eyes:"normal"});
hong({mouth:"0_shock", eyes:"0_shock"});
attack("18p", "alone");
publish("hp_show");
```

(...2500)

`_.fifteencigs = true`

n: ТЫ ИСПОЛЬЗОВАЛ *СТРАХ БЫТЬ НЕЛЮБИМЫМ*

(#act1b)

# act1a_productive

```
bb({body:"normal", mouth:"small", eyes:"normal"});
hong({body:"0_sammich"});
```

b: Вытаскивай свой ноутбук и поработай прямо сейчас!

`hong({eyes:"0_annoyed"})`

h: Эм, я бы предпочла не сорить крошками в свою клавиату--

```
bb({mouth:"normal", eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Если мы не вносим вклад в развитие общества, то мы - его паразиты!

b: Общественное тело отправится к общественному врачу за лекарствами, чтобы убить его общественных паразитов и тогда мы--

```
bb({body:"panic", mouth:"normal", eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: УМРЁЁЁЁЁЁЁЁЁЁЁЁЁЁЁЁЁМ

```
bb({body:"normal", mouth:"normal", eyes:"normal"});
hong({mouth:"0_shock", eyes:"0_shock"});
attack("18p", "bad");
publish("hp_show");
```

(...2500)

`_.parasite = true`

n: ТЫ ИСПОЛЬЗОВАЛ *СТРАХ БЫТЬ ПЛОХИМ ЧЕЛОВЕКОМ*

(#act1b)

# act1a_bread

```
bb({body:"normal", mouth:"normal", eyes:"fear"});
hong({body:"0_sammich", eyes:"0_annoyed"});
```

h: Эти исследования были воспроизвед--

```
bb({body:"fear", mouth:"normal", eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Обработанная пшеница повысит уровень сахара в крови, из-за чего им придется ампутировать все наши конечности, и тогда мы-

`bb({body:"panic"})`

b: УМРЁЁЁЁЁЁЁЁЁЁЁЁЁЁЁЁЁМ

```
bb({body:"normal", mouth:"normal", eyes:"normal"});
hong({mouth:"0_shock", eyes:"0_shock"});
attack("18p", "harm");
publish("hp_show");
```

(...2500)

`_.whitebread = true`

n: ТЫ ИСПОЛЬЗОВАЛ *СТРАХ ВРЕДА*

(#act1b)

# act1b

n: ЭТО СУПЕР ЭФФЕКТИВНО

`bb({mouth:"smile", eyes:"smile"});`

b: Видишь, человек? Я твой верный волк-защитник!

`bb({body:"pride_talk"});`

b: Доверься нутру! Твои чувства всегда верны!

`bb({body:"pride"});`

n: ОПУСТИ УРОВЕНЬ ЭНЕРГИИ ТВОЕГО ЧЕЛОВЕКА ДО НУЛЯ

n: ЧТОБЫ ЗАЩИТИТЬ ЕГО ФИЗИЧЕСКИЕ + СОЦИАЛЬНЫЕ + МОРАЛЬНЫЕ НУЖДЫ, ТЫ МОЖЕШЬ ИСПОЛЬЗОВАТЬ:

n: СТРАХ *ВРЕДА* #harm#

n: СТРАХ *БЫТЬ НЕЛЮБИМЫМ* #alone#

n: И СТРАХ *БЫТЬ ПЛОХИМ ЧЕЛОВЕКОМ* #bad#

`Game.OVERRIDE_TEXT_SPEED = 1.25;`

n4: СОВЕТ: ВЫБИРАЙ ТО, ЧТО ЛИЧНО ЗАДЕВАЕТ ТВОИ ГЛУБОКИЕ, ТЁМНЫЕ СТРАХИ!~

h: ...

```
hong({body:"putaway"});
sfx("rustle");
bb({body:"normal", mouth:"normal", eyes:"normal"});
```

(...1000)

`Game.OVERRIDE_TEXT_SPEED = 1.5;`

h: Знаешь что, думаю пора проверить мой телефон.

```
sfx("rustle2");
hong({body:"phone1", mouth:"neutral", eyes:"neutral"})
```

n: ЗАЩИТИ ТВОЕГО ЧЕЛОВЕКА

n: ОТ МИРА. ОТ ЛЮДЕЙ. ОТ НЕГО САМОГО.

n: УДАЧИ

(...500)

`Game.clearText()`

(...500)

(#act1c)

# act1c

`music('battle', {volume:0.5})`

n: РАУНД ПЕРВЫЙ:
*В БОЙ!*

`bb({body:"normal", mouth:"normal", eyes:"normal"});`

h: Хм. В ленте Facebook говорится, что в эти выходные будет вечеринка.

`bb({eyes:"uncertain"});`

b: Разве этот чудак не устраивает вечеринки *каждые* выходные?

`bb({eyes:"uncertain_right"});`

b: Какую внутреннюю пустоту они пытаются заполнить? Они, должно быть, внутренне очень испорчены!

`hong({eyes:"surprise"});`

h: И ещё, я получила приглашение?

`bb({eyes:"fear", mouth:"normal"});`

b: Что ж!

[Скажи да, или мы умрём от одиночества!](#act1c_loner)

[Скажи нет, там полно ядовитых наркотиков!](#act1c_drugs)

[Проигнорируй, мы только портим все вечеринки.](#act1c_sad)

# act1c_loner

{{if _.fifteencigs}}
b: Пятнадцать сигарет в день, человек! Пятнадцать!
{{/if}}

{{if !_.fifteencigs}}
`Game.OVERRIDE_TEXT_SPEED = 1.5;`
{{/if}}

{{if !_.fifteencigs}}
b: Тогда никто не появится на наших похоронах, они выбросят наш пепел в океан, нас проглотит кит,
{{/if}}

{{if !_.fifteencigs}}
b: и мы станем КИТОВЬЕЙ КАКАШКОЙ!
{{/if}}

{{if !_.fifteencigs}} `_.whalepoop = true` {{/if}}

(...500)

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "alone");
```

(...2500)

`bb({eyes:"normal"});`

{{if !_.fifteencigs}}
b: Так что да, нам стоит пойти на эту вечеринку!
{{/if}}

{{if _.parasite}}
b: Просто принеси ноутбук, чтобы мы могли работать и не быть общественным паразитом.
{{/if}}

{{if _.whitebread}}
b: Если, конечно, они не подают БЕЛЫЙ ХЛЕБ
{{/if}}

`hong({mouth:"anger", eyes:"anger"});`

h: БОЖЕ. Если это заставит тебя заткнуться, то ладно.

h: Я скажу "да".

{{if _.whalepoop}}
b: Китовья какашка, человек! Китовья какашка!
{{/if}}

`_.partyinvite="yes"`

(#act1d)

# act1c_drugs

`bb({mouth:"small", eyes:"fear"});`

{{if _.whitebread}}
b: или даже хуже... БЕЛЫМ ХЛЕБОМ
{{/if}}

{{if _.whitebread}}
`Game.OVERRIDE_TEXT_SPEED = 1.5;`
{{/if}}

{{if _.whitebread}}
b: Мы проглотим так много мета и белого хлеба, что они не смогут поместить наш жирный труп в печь для кремации!
{{/if}}

{{if !_.whitebread}}
b: Мы проглотим так много наркоты, что гробовщик будет удивляться, как наше тело *уже* забальзамировалось!
{{/if}}

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "harm");
```

(...2500)

{{if _.parasite}}
b: Кроме того, мы не можем веселиться, нам нужно работать, иначе мы - ужасные общественные паразиты!
{{/if}}

`hong({mouth:"anger", eyes:"anger"});`

h: БОЖЕ. Если это заставит тебя заткнуться, то ладно.

h: Я скажу "нет".

`_.partyinvite="no"`

(#act1d)

# act1c_sad

`bb({eyes:"uncertain_right", mouth:"normal"});`

`Game.OVERRIDE_TEXT_SPEED = 1.5;`

{{if _.fifteencigs}}
b: Всё, что мы делаем, так это плачем в углу о том, как одиночество настолько же смертельно, как и 15 сигарет в день.
{{/if}}

{{if _.parasite}}
b: Всё, что мы делаем на вечеринках, так это беспокоимся о том, что вместо этого мы должны быть продуктивными.
{{/if}}

{{if _.whitebread}}
b: Всё, что мы делаем, так это беспокоимся о том, как вредная еда может нас убить.
{{/if}}

```
bb({mouth:"normal", eyes:"normal"});
hong({mouth:"neutral", eyes:"lookaway"});
```

h: Интересно, почему.

`hong({eyes:"neutral"});`

`Game.OVERRIDE_TEXT_SPEED = 1.5;`

b: Поэтому, если мы пойдём, то заставим их чувствовать себя плохо, но если мы отклоним их приглашение, то также заставим их чувствовать себя плохо!

`bb({body:"fear", eyes:"fear"});`

`Game.OVERRIDE_TEXT_SPEED = 1.5;`

b: ВСЁ, ЧТО МЫ ДЕЛАЕМ, ТАК ЭТО ЗАСТАВЛЯЕМ ДРУГИХ ЧУВСТВОВАТЬ СЕБЯ ПЛОХО, ПОЭТОМУ МЫ ДОЛЖНЫ ЧУВСТВОВАТЬ СЕБЯ ПЛОХО

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "bad");
```

(...2500)

`hong({mouth:"anger", eyes:"anger"});`

h: Ох. Если это заставит тебя заткнуться, то ладно.

h: Проигнорирую приглашение.

`_.partyinvite="ignore"`

(#act1d)

# act1d

```
bb({body:"normal", mouth:"normal", eyes:"normal"});
hong({mouth:"neutral", eyes:"annoyed"});
```

h: Ладно. Facebook для меня слишком. Мне нужно что-то поспокойнее, менее тревожное.

`hong({eyes:"neutral"});`

h: Что нового в Twitter?

`bb({eyes:"look"});`

[О нет, взгляни на эту ужасную историю в новостях!](#act1d_news)

[О нет, эти твиты случаем не о *нас?*](#act1d_subtweet)

[Хэй, GIF-ка с котиком, лакающим молочко](#act1d_milk)


# act1d_news

```
bb({eyes:"pained1"});
music(null, {fade:2});
```

b: Боже, будто весь мир в огне, не так ли?

```
bb({eyes:"pained2"});
hong({mouth:"sad", eyes:"sad"});
```

b: Такое ощущение, что всему конец, как будто всё умирает, и мы обречены, и мы ничего не можем с этим поделать.

```
Game.OVERRIDE_TEXT_SPEED = 0.5;
bb({mouth:"shut"});
```

b: ...

`bb({mouth:"smile", eyes:"smile"});`

b: Давай ретвитнем это!

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "harm");
```

(...2500)

`_.badnews=true`

```
music('battle', {volume:0.5});
hong({mouth:"anger", eyes:"anger"});
bb({body:"normal", mouth:"normal", eyes:"normal"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: Ладно, я ретвитну, просто успокойся!

`hong({mouth:"neutral", eyes:"annoyed"});`

h: К чёрту. Загляну-ка в Snapchat.

(#act1e)


# act1d_subtweet

`bb({eyes:"fear"});`

b: Это сабтвит! Подлый, подлый сабтвит!

`hong({eyes:"annoyed"});`

h: Может и нет?

`bb({eyes:"narrow", mouth:"small"});`

b: Но что, если они все говорят за нашей спиной

h: Они не--

`bb({body:"fear", eyes:"fear", mouth:"normal"});`

b: ПРЯМО ЗА НАШЕЙ СПИНОЙ

`hong({eyes:"sad", mouth:"sad"});`

h: Я не--

`bb({eyes:"narrow", mouth:"small"});`

b: Но *вдруг*

h: П--

`bb({eyes:"narrow_eyebrow"});`

b: *вдруг*

```
Game.OVERRIDE_TEXT_SPEED = 0.5;
hong({mouth:"shut"});
```

h: ...

(...1000)

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "alone");
```

(...2500)

`_.subtweet=true`

```
hong({mouth:"anger", eyes:"annoyed"});
bb({body:"normal", mouth:"normal", eyes:"normal"});
```

h: О-КЕЙ, попробую Snapchat.

(#act1e)

# act1d_milk

`hong({mouth:"smile", eyes:"neutral"});`

h: Хех, да, это довольно мило, только что ретвитнула, я ду--

```
hong({mouth:"shock", eyes:"shock"});
bb({body:"scream"});
Game.OVERRIDE_TEXT_SPEED = 1.8;
```

b: КОШКИ НЕ ПЕРЕВАРИВАЮТ МОЛОКО, И МЫ - УЖАСНЫЕ ЛЮДИ, НАСЛАЖДАЮЩИЕСЯ НАСИЛИЕМ НАД ЖИВОТНЫМИ

```
bb({body:"normal", mouth:"normal", eyes:"fear"});
attack("18p", "bad");
```

(...2500)


`_.catmilk=true`

```
hong({mouth:"anger", eyes:"annoyed"});
bb({body:"normal", mouth:"normal", eyes:"normal"});
```

h: О-КЕЙ, попробую Snapchat.

(#act1e)

# act1e

`hong({mouth:"neutral", eyes:"neutral"});`

h: Хм, фотки с вчерашней ночи. Так *вот* какие эти еженедельные вечеринки.

{{if _.partyinvite=="yes"}} (#act1e_said_yes) {{/if}}

{{if _.partyinvite=="no"}} (#act1e_said_no) {{/if}}

{{if _.partyinvite=="ignore"}} (#act1e_said_ignore) {{/if}}

# act1e_said_yes

`hong({mouth:"sad", eyes:"annoyed"});`

h: Уф, выглядит слишком многолюдно для меня.

h: Может, мне не следовало соглашаться на приглашение?

```
hong({mouth:"neutral", eyes:"neutral"});
bb({mouth:"normal", eyes:"normal"});
```

[Поменять наш ответ? Как придурок?!](#act1e_yes_dontchange)

[Измени наш ответ! Слишком многолюдно!](#act1e_yes_changetono)

{{if _.subtweet}}
[Мда, они правда твитили о нас.](#act1e_ignore_subtweet)
{{/if}}

{{if _.badnews}}
[Погоди, мы ретвитнули без фактчекинга.](#act1e_ignore_factcheck)
{{/if}}

{{if (!_.subtweet && !_.badnews)}}
[Ты знаешь, что у тебя и вправду плохая осанка?](#act1e_ignore_posture)
{{/if}}

# act1e_yes_dontchange

```
bb({eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Они рассчитывали, что мы приедём, и теперь мы предаём их доверие? Ты хочешь умереть в одиночестве?!

{{if _.fifteencigs}}
b: ПЯТНАДЦАТЬ. СИГАРЕТ.
{{/if}}

{{if _.whalepoop}}
b: КИТОВЬЯ. КАКАШКА.
{{/if}}

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "alone");
```

(...2500)

```
hong({mouth:"anger", eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: Заткнись, заткнись, я пойду туда!

(#act1f)

# act1e_yes_changetono

```
bb({eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Разве ты не знаешь о людских давках?

```
bb({body:"fear", mouth:"small", eyes:"narrow"});
hong({eyes:"sad", mouth:"sad"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: В 2003 году в ночном клубе на Род-Айленде произошел пожар, и паника заставила толпу людей заблокировать выходы,

b: в результате чего 100 человек сгорели до смерти.
```
bb({body:"normal", mouth:"normal", eyes:"fear"});
hong({mouth:"shock"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: ТЫ ХОЧЕШЬ ЧТОБЫ ЭТО СЛУЧИЛОСЬ С НАМИ-

```
bb({body:"scream"});
Game.OVERRIDE_TEXT_SPEED = 2.5;
```

b: СКАЖИ НЕТ СКАЖИ НЕТ СКАЖИ НЕТ СКАЖИ НЕТ СКАЖИ НЕТ СКАЖИ НЕТ СКАЖИ Н-


```
bb({body:"normal", eyes:"fear", mouth:"normal"});
hong({mouth:"shock", eyes:"shock"});
attack("18p", "harm");
```

(...2500)

```
hong({eyes:"anger", mouth:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: Заткнись, заткнись, я не пойду туда, не пойду! Боже!

(#act1f)

# act1e_said_no

`hong({mouth:"sad", eyes:"sad"});`

h: Хм... выглядит довольно весело.

h: Может, мне не стоило отказываться от приглашения?

`bb({mouth:"normal", eyes:"normal"});`

[Изменить свой ответ? Как ^мудак^?!](#act1e_no_dontchange)

[Поменяй ответ! Не умирай одиноким!](#act1e_no_changetoyes)

{{if _.subtweet}}
[Мда, они действительно обсуждали нас.](#act1e_ignore_subtweet)
{{/if}}

{{if _.badnews}}
[Погоди, мы ретвитнули без проверки фактов.](#act1e_ignore_factcheck)
{{/if}}

{{if (!_.subtweet && !_.badnews)}}
[Ты знаешь, что у тебя действительно плохая осанка?](#act1e_ignore_posture)
{{/if}}

# act1e_no_dontchange

`bb({eyes:"anger"})`

b: Все рассчитывали на нас!

b: ...оставить их в покое и позволить им устроить хорошую вечеринку без ужасного отвратительного {{if _.whitebread}}жующего-белый-хлеб{{/if}} подонка, как ты----


```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "bad");
```

(...2500)

```
bb({body:"normal", eyes:"uncertain", mouth:"normal"});
hong({mouth:"anger", eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: Заткнись, заткнись, я не пойду туда!

(#act1f)

# act1e_no_changetoyes

```
bb({body:"fear", eyes:"fear", mouth:"normal"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Хроническое одиночество увеличивает уровень кортизола, а также риск сердечно-сосудистых заболеваний и инсульта!

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "harm");
```

(...2500)

{{if _.fifteencigs}}
b: ПЯТНАДЦАТЬ. СИГАРЕТ.
{{/if}}

```
bb({body:"normal", eyes:"normal", mouth:"normal"});
hong({mouth:"anger", eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: Заткнись, заткнись, я пойду туда, пойду! Боже!

(#act1f)

# act1e_ignore_subtweet

```
bb({eyes:"fear", mouth:"small"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Все наши проблемные твиты вернулись к нам!

```
bb({body:"fear", eyes:"fear", mouth:"normal"});
Game.OVERRIDE_TEXT_SPEED = 1.7;
```

b: Нас призовут к ответу, отвергнут и будут тащить на веревке верхом по информационной магистрали!

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "alone");
```

(...2500)

```
bb({body:"normal", eyes:"normal", mouth:"normal"});
hong({mouth:"anger", eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: Да что с тобой не так?!

(#act1f)

# act1e_ignore_factcheck

```
bb({eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Мы распространяем дезинформацию! Мы уничтожаем доверие к свободным СМИ!

```
bb({body:"scream"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Мы - причина, по которой фашизм восстанет из обломков демократии!

```
bb({body:"normal", eyes:"anger"});
hong({mouth:"shock", eyes:"shock"});
attack("18p", "bad");
```

(...2500)

```
hong({mouth:"anger", eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
_.factcheck = true;
```

h: Да что с тобой не так?!

(#act1f)

# act1e_ignore_posture

```
bb({eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Хочешь иметь позвоночник в виде кренделя?! Хватит сутулиться за экраном!

```
bb({body:"meta"});
```

b: Тебя это тоже касается.

```
bb({body:"normal", mouth:"normal"});
hong({mouth:"shock", eyes:"shock"});
attack("18p", "harm");
```

(...2500)

```
bb({body:"normal", eyes:"normal", mouth:"normal"});
hong({mouth:"anger", eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: Да что с тобой не так?!

(#act1f)

# act1e_said_ignore

`hong({mouth:"sad", eyes:"sad"});`

h: Хм... выглядит довольно весело.

h: Может, мне не стоило игнорировать приглашение?

`bb({mouth:"normal", eyes:"normal"});`

[Игнорируй, мы недостаточно хороши для вечеринок.](#act1e_ignore_continue)

[А вообще, скажи "да"](#act1e_ignore_changetoyes)

[А вообще, скажи "нет"](#act1e_ignore_changetono)

# act1e_ignore_continue

`hong({eyes:"annoyed"});`

h: Разве продолжать игнорировать их не слишком грубо?

`bb({eyes:"normal_right"});`

b: Ну, другие люди всегда игнорируют *нас*, так что

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "alone");
```

(...2500)

`bb({eyes:"normal"});`

b: Давай ответим им тем же.

(#act1f)

# act1e_ignore_changetoyes

`hong({eyes:"surprise", mouth:"smile"});`

h: Ты... позволишь мне повеселиться?

b: Ну, одиночество всё же *может* убить нас.

`hong({eyes:"neutral", mouth:"neutral"});`

(#act1e_no_changetoyes)

# act1e_ignore_changetono

`bb({eyes:"narrow"});`

b: Слишком многолуюно. Толпы опасны.

(#act1e_yes_changetono)


# act1f

```
hong({mouth:"neutral", eyes:"neutral"});
bb({body:"normal", mouth:"normal", eyes:"normal"});
```

h: Неважно. Новое уведомление из Tinder.

`bb({eyes:"uncertain"})`

b: Чего, это то приложение для секс-знакомств?

`hong({eyes:"annoyed"})`

h: Это не приложение для секс-знакомств, просто способ узнать новых люд--

`bb({eyes:"narrow"})`

b: Это приложение для секс-знакомств.

```
hong({eyes:"surprise", mouth:"smile"});
bb({eyes:"normal"});
```

h: О, мне кого-то нашли! Он такой милый!

```
bb({eyes:"narrow_eyebrow"});
hong({eyes:"sad", mouth:"anger"})
```

h: Пожалуйста, не испорть м--

```
bb({body:"panic"});
Game.OVERRIDE_TEXT_SPEED = 2.0;
```

b: ОПАСНОСТЬ ОПАСНОСТЬ ОПАСНОСТЬ ОПАСНОСТЬ ОПАСНОСТЬ ОПАСНОСТЬ

`bb({body:"fear", eyes:"fear", mouth:"normal"})`

[Нас *используют* другие люди.](#act1f_used_by_others)

[Мы *используем* других людей.](#act1f_using_others)

[ОН СЕРИЙНЫЙ УБИЙЦА](#act1f_killer)

# act1f_used_by_others

`bb({body:"point_crotch", eyes:"normal", mouth:"normal"})`

b: Случайные секс-знакомства могут заполнить дыру здесь,

b: но они никогда не смогут заполнить дыру...

`bb({body:"point_heart", eyes:"pretty", mouth:"small"})`

b: *здесь*.

(...1000)

```
bb({body:"normal", mouth:"normal", eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Суть в том, что МЫ УМРЁМ В ОДИНОЧЕСТВЕ

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "alone");
```

(...2500)

`_.hookuphole=true`

(#act1g)

# act1f_using_others

`bb({eyes:"narrow", mouth:"small"})`

b: Ты думаешь, что гениталии других людей - это покемоны, которых мы собираем?

```
bb({body:"sing", eyes:"pretty", mouth:"shut"});
music("pokemon");
Game.clearText();
Game.FORCE_CANT_SKIP = true;
```

```
Game.FORCE_TEXT_DURATION = 1000;
Game.FORCE_NO_VOICE = true;
```

b: ♫ [ЗАГЛАВНАЯ ТЕМА ПОКЕМОНОВ]-

(...5600)

```
bb({mouth:"normal"});
Game.FORCE_TEXT_DURATION = 2400;
```

b: ♫ Услыхав судьбы призыв-

(...500)

```
bb({eyes:"narrow", mouth:"small"});
Game.FORCE_TEXT_DURATION = 2100;
```

b: ♫ ЗАХОТЕЛА СТАТЬ ^ШЛЮХОЙ^ Я-

(...1500)

```
bb({eyes:"pretty"});
Game.FORCE_TEXT_DURATION = 2300;
```

b: ♫ БЁДРА и ^ЖОПА^, ПЫШНАЯ ГРУДЬ-

(...500)

```
bb({eyes:"fear", mouth:"normal"});
Game.FORCE_TEXT_DURATION = 2000;
```

b: ♫ И ПОТНЫЙ ^*ХУЙ*^ ДЛЯ МЕНЯ!- 

(...1000)

```
bb({eyes:"smile", mouth:"smile"});
Game.FORCE_TEXT_DURATION = 1000;
```

b: ♫ СЕКСО-МОН! МЫ СМО-

```
Game.FORCE_CANT_SKIP = false;
Game.clearText();
music(false);
bb({body:"normal", mouth:"normal", eyes:"normal"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Короче, суть в том, что мы - манипуляторы.

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "bad");
```

(...2500)

`_.pokemon=true`

(#act1g)

# act1f_killer

`Game.OVERRIDE_TEXT_SPEED = 1.5;`

{{if _.whitebread}}
b: Он заманит тебя в ловушку и принудительно откормит тебя белым хлебом, чтобы он мог носить твою кожу как костюм!
{{/if}}

{{if _.parasite}}
b: Он забьёт тебя таймером помодоро и скажет: "ТЫ ДОЛЖЕН БЫТЬ ПРОДУКТИВНЫМ, ТЫ ПАРАЗИТ"
{{/if}}

{{if !_.whitebread && !_.parasite}}
b: Он разорвёт твоё тело на кровавое конфетти, превратит твои внутренности в гирлянды и намешает твою кровь в чаше для пунша!
{{/if}}

{{if !_.whitebread && !_.parasite}}
b: Как тебе ТАКОЕ приглашение на вечеринку?!
{{/if}}

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "harm");
```

(...2500)

`_.serialkiller=true`

(#act1g)

# act1g

```
bb({body:"normal", mouth:"normal", eyes:"look"});
hong({body:"2_tired"});
Game.OVERRIDE_TEXT_SPEED = 0.5;
music(false);
```

h: ...

(...500)

h: Я так устала от этой игры.

(...700)

`Game.OVERRIDE_TEXT_SPEED = 1.5;`

h:
{{if _.fifteencigs}}"одиночество убьёт нас"... {{/if}}
{{if _.parasite}}"мы социальные паразиты"... {{/if}}
{{if _.whitebread}}"не ешь это, оно нас убьёт"... {{/if}}
{{if _.subtweet}}"они говорят за нашими спинами"... {{/if}}
{{if _.badnews}}"мир в огне"... {{/if}}
{{if _.hookuphole}}"мы умрём в одиночестве"... {{/if}}
{{if _.serialkiller}}"он - серийный убийца"... {{/if}}
{{if _.catmilk}}"кошки не переваривают молоко"... {{/if}}
{{if _.pokemon}}^хреновая^ пародийная песня... {{/if}}

h: Я просто хочу жить своей жизнью.

h: Я просто хочу освободиться от всей этой... боли.

`bb({eyes:"look_sad"});`

b: Хэй... человек...

`Game.OVERRIDE_TEXT_SPEED = 0.5;`

b: Всё будет хорошо.

(...600)

`bb({body:"point_heart", eyes:"look_sad_smile", mouth:"smile"});`

b: Как твой верный волк-защитник, я всегда буду начеку и сделаю всё возможное, чтобы ты был в безопасности.

`bb({body:"normal", eyes:"look_sad", mouth:"smile"});`

b: Даю слово.

(...600)

```
bb({body:"normal", eyes:"normal", mouth:"normal"});
hong({body:"phone1", eyes:"neutral", mouth:"neutral"});
```

h: Последнее приложение. Instagram. Что же ты мне дашь?

`hong({eyes:"sad"});`

h: Это... больше фоток с вечеринок.

`hong({mouth:"sad"});`

h: Все выглядят такими счастливыми. Свободные от забот. Свободные от тревоги.

`hong({mouth:"anger"});`

h: Боже, почему я не могу быть, как они? Почему я не могу просто быть *нормальной?*

`bb({eyes:"normal_right"});`

b: Говоря о вечеринках, вспомни то приглашение. Вот моё ФИНАЛЬНОЕ решение:

`bb({eyes:"normal"});`

[Нам следует пойти.](#act1g_go) `Game.OVERRIDE_CHOICE_LINE=true`

[Нам не следует идти.](#act1g_dont) `Game.OVERRIDE_CHOICE_LINE=true`

# act1g_go

`_.act1g = "go"`

(#act1h)

# act1g_dont

`_.act1g = "dont"`

(#act1h)

# act1h

b: Нам сл--

```
bb({eyes:"wat", mouth:"small"});
hong({body:"2_fuck"});
```

h: ИДИ.

`hong({body:"2_you"});`

h: *^НАХУЙ^.*

(...500)

b: ч

(...1500)

`bb({eyes:"wat_2"});`

b: чего?

`hong({body:"phone1", eyes:"anger", mouth:"anger"});`

h: Я ПОЙДУ на эту вечеринку,

{{if _.act1g=="go"}}
h: и НЕ потому, что ты так хочешь, а потому, что *Я* так хочу.
{{/if}}

{{if _.act1g=="dont"}}
h: Именно ПОТОМУ, что ты не хочешь.
{{/if}}

```
hong({body:"putaway"});
sfx("rustle");
```

h: Ты НЕ контролируешь меня.

```
sfx("rustle2");
hong({body:"0_sammich", eyes:"0_annoyed", mouth:"0_neutral"});
```

h: А теперь извини, я съем этот вкуснейший сэндвич в этом ^блядском^ месте.

`hong({body:"2_sammich_eat"});`

(...601)

```
sfx("sandwich");
hong({body:"2_sammich_eaten", eyes:"0_lookaway", mouth:"0_chew1"})
```

(...601)

```
bb({body:"normal", eyes:"uncertain", mouth:"shut"});
Game.OVERRIDE_TEXT_SPEED = 0.5;
```

b: ...

```
bb({eyes:"normal_right"});
Game.OVERRIDE_TEXT_SPEED = 1;
```

b: ...

```
bb({eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 4;
```

b: ..................

(...500)

`bb({mouth:"normal"});`

[ААААА МЫ УМРЁМ](#act1h_death) `Game.OVERRIDE_CHOICE_LINE = true;`

[ААААА ВСЕ НАС НЕНАВИДЯТ](#act1h_loneliness) `Game.OVERRIDE_CHOICE_LINE = true;`

[ААААА МЫ УЖАСНЫЕ ЛЮДИ](#act1h_worthless) `Game.OVERRIDE_CHOICE_LINE = true;`

# act1h_death

```
bb({body:"fear"});
Game.OVERRIDE_TEXT_SPEED = 3;
```

b: ААААА МЫ УМРЁМ ААААААААААААА

```
hong({body:"3_defeated1"});
attack("100p", "harm");
```

(...2500)

(#act1i)

# act1h_loneliness

```
bb({body:"fear"});
Game.OVERRIDE_TEXT_SPEED = 3;
```

b: ААААА ВСЕ НАС НЕНАВИДЯТ ААААААААААААА

```
hong({body:"3_defeated1"});
attack("100p", "alone");
```

(...2500)

(#act1i)

# act1h_worthless

```
bb({body:"fear"});
Game.OVERRIDE_TEXT_SPEED = 3;
```

b: ААААА МЫ УЖАСНЫЕ ЛЮДИ ААААААААААААА

```
hong({body:"3_defeated1"});
attack("100p", "bad");
```

(...2500)

(#act1i)

# act1i

```
bb({mouth:"smile_lock", eyes:"smile", body:"normal"});
music('battle', {volume:0.5});
```

n: ПОЗДРАВЛЯЕМ

(...500)

n: ТЫ УСПЕШНО ЗАЩИТИЛ ФИЗИЧЕСКИЕ + СОЦИАЛЬНЫЕ + МОРАЛЬНЫЕ НУЖДЫ ТВОЕГО ЧЕЛОВЕКА

n: ПОСМОТРИ, КАК ОН ТЕБЕ БЛАГОДАРЕН!

(...500)

n: ТЕПЕРЬ, КОГДА ЕГО ЭНЕРГИЯ НА НУЛЕ, ТЫ МОЖЕШЬ КОНТРОЛИРОВАТЬ ЕГО ДЕЙСТВИЯ

`bb({mouth:"smile", eyes:"normal"});`

n: ВЫБЕРИ СВОЙ ЗАВЕРШАЮЩИЙ ХОД

`bb({mouth:"small_lock", eyes:"fear"});`

n: *ДОБЕЙ ЕГО*

[{БОРЬБА: Наказать свой стрессовый телефон!}](#act1i_phone) `Game.OVERRIDE_CHOICE_LINE=true`

[{ОТСТУПЛЕНИЕ: Свернуться в клубок и плакать!}](#act1i_cry) `Game.OVERRIDE_CHOICE_LINE=true`

# act1i_phone

`bb({mouth:"normal", eyes:"narrow"})`

b: Твой телефон заставляет тебя паниковать!

`bb({eyes:"anger"})`

b: Цукерберк и другие корпорации перерабатывают твоё ментальное здоровье в деньги венчурных капиталистов!

```
bb({body:"fear", eyes:"fear"});
hong({body:"3_defeated2"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Накажи свой телефон! Уничтожь его! Убей его!

```
Game.OVERRIDE_TEXT_SPEED = 2.5;
bb({body:"flail"});
hong({body:"3_defeated3"});
_.act1_ending = "fight";
```

b: УБЕЙ ЕГО УБЕЙ ЕГО УБЕЙ ЕГО УБЕЙ ЕГО УБЕЙ ЕГО УБЕЙ ЕГО УБЕЙ ЕГО УБЕЙ ЕГО УБЕЙ ЕГО УБЕЙ ЕГО УБЕЙ ЕГО УБЕЙ ЕГО УБЕЙ ЕГО УБЕЙ Е--

(#act1j)

# act1i_cry

`bb({eyes:"fear", mouth:"normal"})`

b: Весь мир полон опасностей!

```
bb({body:"fear"});
hong({body:"3_defeated2"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Действуй как броненосец! Свернись в клубок для самообороны!

```
Game.OVERRIDE_TEXT_SPEED = 2.5;
bb({body:"flail"});
hong({body:"3_defeated3"});
_.act1_ending = "flight";
```

b:СВЕРНИСЬ И ПЛАЧЬ СВЕРНИСЬ И ПЛАЧЬ СВЕРНИСЬ И ПЛАЧЬ СВЕРНИСЬ И ПЛАЧЬ СВЕРНИСЬ И ПЛАЧЬ СВЕРНИСЬ И ПЛ--

(#act1j)

# act1j

`SceneSetup.act1_outro()`