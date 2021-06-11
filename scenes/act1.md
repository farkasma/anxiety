# act1

```
SceneSetup.act1();
```

(...300)

n: ÉS EZ ITT AZ EMBER SZORONGÁSA

n: _TE_ VAGY A SZORONGÁS

{{if window.localStorage.continueChapter=="replay"}}
(#act1_replay)
{{/if}}

{{if window.localStorage.continueChapter!="replay"}}
(#act1_normal)
{{/if}}



# act1_replay

`hong({mouth:"0_neutral", eyes:"0_neutral"})`

h: Ó, helló! Megint itt vagyunk?

`hong({eyes:"0_neutral"})`

n: A FELADATOD MEGVÉDENI AZ EMBERT A *VESZÉLYTŐL*

`bb({eyes:"look", mouth:"small_lock"})`

n: IGAZÁBÓL A JÁTÉK ÚJRAJÁTSZÁSA MOST IS *VESZÉLYBE* SODORJA ŐT

n: GYORSAN, FIGYELMEZTESD!

```
sfx("squeak");
bb({body:"squeeze_talk"});
hong({body:"0_squeeze"});
```

b: Ember! Figyelj, veszélyben vagyunk! A játékos...

[...újra kínozni fog minket](#act1_replay_torture)

[...nem fog alternatív befejezést találni!](#act1_replay_alternate)

[...ludonarratív disszonanciát fog kapni!](#act1_replay_dissonance)

# act1_replay_torture

```
window.HACK_REPLAY = JSON.parse(localStorage.act4);
bb({body:"normal", mouth:"normal", eyes:"fear"});
hong({body:"0_sammich"});
```

{{if window.HACK_REPLAY.act1_ending=="fight"}}
b: Összegömbölyítenek minket egy kis labdává és megríkatnak!
{{/if}}

{{if window.HACK_REPLAY.act1_ending=="flight"}}
b: Megöletik velünk a telefonod, mert pánikrohamot okoz neked!
{{/if}}

{{if window.HACK_REPLAY.a2_ending=="fight"}}
b: *NEM* üttetik meg velünk a buli szervezőjét!
{{/if}}

{{if window.HACK_REPLAY.a2_ending=="flight"}}
b: Megüttetik velünk a buli Szimpatikus Antihős házigazdáját!
{{/if}}

{{if window.HACK_REPLAY.a3_ending=="jump"}}
h: Legalább ezúttal lehet nem ugrunk le a te--
{{/if}}

{{if window.HACK_REPLAY.a3_ending=="walkaway"}}
b: LEUGRASZTANAK MINKET A TETŐRŐL.
{{/if}}

`bb({body:"fear"});`

b: AZ A SOK BORZASZTÓ DOLOG, AMIT VELÜNK TESZ MAJD, ÉS AZTÁN MI--

(#act1_replay_end)


#act1_replay_alternate

```
bb({body:"normal", mouth:"normal", eyes:"fear"});
hong({body:"0_sammich"});
```

h: Sure, the story as a *whole* is the same, but each chapter has two possible endings, plus all the branching dialogue opti--

`bb({body:"fear"});`

b: A játékos csalódott lesz. Bezárja ezt a böngészőlapot, kitörli a programunkat, és aztán mi--

(#act1_replay_end)


# act1_replay_dissonance

```
bb({body:"normal", mouth:"normal", eyes:"fear"});
hong({body:"0_sammich"});
```

h: Hogy lúd-micsodát?

`bb({eyes:"normal"});`

b: A történet arról szólt, hogy hogyan *DÖNTESZ* a félelmeddel való egészséges együttműködés mellett,

`bb({eyes:"normal_right"});`

b: De a játék újrajátszása ugyanazt a történetet fogja mutatni, ezzel azt mutatva, hogy a *DÖNTÉSEID* nem számítanak,

`bb({eyes:"narrow_eyebrow"});`

b: Ezáltal ellentmondásba keveredve a játék üzenete és játékmenete között,

`bb({eyes:"fear"});`

b: Ezáltal lebontva ezen univerzum narratív szövetét,

`bb({body:"fear"});`

b: És aztán mi--

(#act1_replay_end)


# act1_replay_end

`bb({body:"panic"})`

b: MEGHALUUUUUUUUUUUUUNK

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

h: Oké, helyezkedjünk újra karakterbe.

```
Game.clearText();
```

n4: (LEGYEN A _TE_ FÉLELMED BLA BLA BLA LEGHASONLÓBB A _TE_ FÉLELMEDHEZ BLA BLA ISMERED A JÁRÁST ERRE FELÉ)

```
sfx("squeak");
hong({body:"0_squeeze"});
bb({body:"squeeze"});
```

(#act1_normal_choice)



# act1_normal

`hong({mouth:"0_neutral", eyes:"0_annoyed"})`

h: Ó, jól van, a farkasom visszatért. Naaaaaagyszerű.

`hong({eyes:"0_neutral"})`

n: A FELADATOD MEGVÉDENI AZ EMBERED A *VESZÉLYTŐL*

`bb({eyes:"look", mouth:"small_lock"})`

n: IGAZÁBÓL AZ A SZENDVICS ÉPPEN MOST IS *VESZÉLYBE* SODORJA ŐT

n: GYORSAN, FIGYELMEZTESD!

```
sfx("squeak");
bb({body:"squeeze_talk"});
hong({body:"0_squeeze"});
```

b: Ember! Figyelj, veszélyben vagyunk! A veszély...

`bb({body:"squeeze"})`

n4: (HAGYD A _SAJÁT_ SZORONGÁSOD JÁTSZANI! VÁLASZD A _TE_ SZORONGÁSODHOZ LEGJOBBAN HASONLÍTÓ VÁLASZT)

(#act1_normal_choice)

# act1_normal_choice

[Egyedül ebédelünk! Már megint!](#act1a_alone) `bb({body:"squeeze_talk"})`

[Ebéd közben nem vagyunk produktívak!](#act1a_productive) `bb({body:"squeeze_talk"})`

[A fehér kenyér rossz nekünk!](#act1a_bread) `bb({body:"squeeze_talk"})`

# act1a_alone

```
bb({body:"normal", mouth:"small", eyes:"narrow"});
hong({body:"0_sammich"});
```

b: Nem tudtad, hogy a magányosságnak legalább annyi köze van a korai halálozáshoz, mint napi 15 cigarettának?-

`Game.OVERRIDE_TEXT_SPEED = 2;`

`bb({mouth:"normal", eyes:"normal_right"})`

b: (Holt-Lunstad 2010, PLoS Medicine)

`hong({eyes:"0_annoyed"})`

h: Öö, köszönöm a forrásmegjelölést, de--

`Game.OVERRIDE_TEXT_SPEED = 2;`

`bb({body:"fear", mouth:"normal", eyes:"fear"})`

b: Ami azt jelenti, hogy ha nem lógunk valakivel most azonnal, akkor-

`bb({body:"panic"})`

b: MEGHALUUUUUUUUUUUUUNK

```
bb({body:"normal", mouth:"normal", eyes:"normal"});
hong({mouth:"0_shock", eyes:"0_shock"});
attack("18p", "alone");
publish("hp_show");
```

(...2500)

`_.fifteencigs = true`

n: A *SZERETET HIÁNYÁTÓL VALÓ FÉLELMET* HASZNÁLTAD

(#act1b)

# act1a_productive

```
bb({body:"normal", mouth:"small", eyes:"normal"});
hong({body:"0_sammich"});
```

b: Kapd elő a laptopod és dolgozz egy kicsit!

`hong({eyes:"0_annoyed"})`

h: Öö, nem igazán szeretnék morzsákat a billenty--

```
bb({mouth:"normal", eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Ha nem teszünk hozzá semmit a társadalomhoz, társadalom-paraziták vagyunk!

b: A társadalom-test elmegy majd a társadalom-orvoshoz gyógyszerért, hogy megölje a társadalom-parazitáit, és akkor mi--

```
bb({body:"panic", mouth:"normal", eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: MEGHALUUUUUUUUUUUUUNK

```
bb({body:"normal", mouth:"normal", eyes:"normal"});
hong({mouth:"0_shock", eyes:"0_shock"});
attack("18p", "bad");
publish("hp_show");
```

(...2500)

`_.parasite = true`

n: *A ROSSZ SZEMÉLYÉ VÁLÁS FÉLELMÉT* HASZNÁLTAD

(#act1b)

# act1a_bread

```
bb({body:"normal", mouth:"normal", eyes:"fear"});
hong({body:"0_sammich", eyes:"0_annoyed"});
```

h: Meg tudták ismételni ezeket a kuta--

```
bb({body:"fear", mouth:"normal", eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: A feldolgozott búza megnöveli a vércukorszintünket, ezért amputálni kell majd az összes végtagunkat, és akkor mi-

`bb({body:"panic"})`

b: MEGHALUUUUUUUUUUUUUNK

```
bb({body:"normal", mouth:"normal", eyes:"normal"});
hong({mouth:"0_shock", eyes:"0_shock"});
attack("18p", "harm");
publish("hp_show");
```

(...2500)

`_.whitebread = true`

n: A *SÉRÜLÉSTŐL VALÓ FÉLELMET* HASZNÁLTAD

(#act1b)

# act1b

n: SZUPERHATÉKONY

`bb({mouth:"smile", eyes:"smile"});`

b: Látod, ember? Én vagyok a hűséges őrző-farkasod!

`bb({body:"pride_talk"});`

b: Hallgass a megérzésedre! Az érzéseid mindig valósak!

`bb({body:"pride"});`

n: VIDD AZ EMBERED ENRGIASZINTJÉT NULLÁRA

n: A FIZIKAI + SZOCIÁLIS + MORÁLIS IGÉNYEIK MEGVÉDÉSÉRE HASZNÁLHATOD:

n: A *SÉRÜLÉSTŐL* VALÓ FÉLELMET #harm#

n: A *SZERETET HIÁNYÁTÓL* VALÓ FÉLELMET #alone#

n: *A ROSSZ SZEMÉLYÉ VÁLÁS* FÉLELMÉT #bad#

`Game.OVERRIDE_TEXT_SPEED = 1.25;`

n4: (PRO-TIP: VÁLASZD A SZEMÉLYES FÉLELMEIDET LEGJOBBAN ELTALÁLÓ LEHETŐSÉGEKET!~)

h: ...

```
hong({body:"putaway"});
sfx("rustle");
bb({body:"normal", mouth:"normal", eyes:"normal"});
```

(...1000)

`Game.OVERRIDE_TEXT_SPEED = 1.5;`

h: tudod mit, azt hiszem itt az ideje megnéznem a telefonomat.

```
sfx("rustle2");
hong({body:"phone1", mouth:"neutral", eyes:"neutral"})
```

n: VÉDD MEG AZ EMEBERED

n: A VILÁGTÓL. MÁS EMBEREKTŐL. MAGUKTÓL.

n: SOK SIKERT

(...500)

`Game.clearText()`

(...500)

(#act1c)

# act1c

`music('battle', {volume:0.5})`

n: ELSŐ KÖR: *HARC!*

`bb({body:"normal", mouth:"normal", eyes:"normal"});`

h: Hmm. A Facebook feed szerint lesz egy buli most hétvégén.

`bb({eyes:"uncertain"});`

b: *Minden* héten tart egy bulit az különc, nem?

`bb({eyes:"uncertain_right"});`

b: Milyen belső űrt próbálhat betölteni? Nagyon el lehet rontva belül!

`hong({eyes:"surprise"});`

h: Egyébként meg is hívtak?

`bb({eyes:"fear", mouth:"normal"});`

b: Na!

[Mondj igent, különben belehalunk a magányba!](#act1c_loner)

[Mondj nemet, tele van mérgező drogokkal](#act1c_drugs)

[Ne is törődj vele, úgyis csak elrontjuk a bulikat.](#act1c_sad)

# act1c_loner

{{if _.fifteencigs}}
b: Tizenöt cigaretta naponta, ember! Tizenöt!
{{/if}}

{{if !_.fifteencigs}}
`Game.OVERRIDE_TEXT_SPEED = 1.5;`
{{/if}}

{{if !_.fifteencigs}}
b: Aztán majd senki nem jön el a temetésünkre, beszórják a hamvainkat a tengerbe, megesz minket egy bálna,
{{/if}}

{{if !_.fifteencigs}}
b: és átváltozunk BÁNA KAKIVÁ!
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
b: Szóval ja, el kéne menned a buliba!
{{/if}}

{{if _.parasite}}
b: Csak hozd a laptopot, hogy tudjunk dolgozni és ne legyünk társadalom-paraziták.
{{/if}}

{{if _.whitebread}}
b: Csakis akkor, ha nem szolgálnak fel FEHÉR KENYERET
{{/if}}

`hong({mouth:"anger", eyes:"anger"});`

h: ISTENEM. Ha így végre befogod, legyen.

h: Igent mondok.

{{if _.whalepoop}}
b: Bálna kaki, ember! Bálna kaki!
{{/if}}

`_.partyinvite="yes"`

(#act1d)

# act1c_drugs

`bb({mouth:"small", eyes:"fear"});`

{{if _.whitebread}}
b: vagy ami még rosszabb... FEHÉR KENYÉR
{{/if}}

{{if _.whitebread}}
`Game.OVERRIDE_TEXT_SPEED = 1.5;`
{{/if}}

{{if _.whitebread}}
b: Annyi meth-en és fehér kenyéren fogunk túladagolni, hogy a dagadt hullánk nem fog beférni a hamvasztó kemencébe!
{{/if}}

{{if !_.whitebread}}
b: Annyi drogon fogunk túladagolni, a halál azon fog gondolkozni, hogyan lehetett a testünk már *előre* bebalzsamozva!
{{/if}}

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "harm");
```

(...2500)

{{if _.parasite}}
b: Amúgysem bulizhatunk, többet kell dolgoznunk, hogy ne legyünk borzasztó társadalom-paraziták!
{{/if}}

`hong({mouth:"anger", eyes:"anger"});`

h: ISTENEM. Ha így végre befogod, legyen.

h: Nemet mondok.

`_.partyinvite="no"`

(#act1d)

# act1c_sad

`bb({eyes:"uncertain_right", mouth:"normal"});`

`Game.OVERRIDE_TEXT_SPEED = 1.5;`

{{if _.fifteencigs}}
b: Folyton csak sírunk a sarokban, hogy a magényosság legalább olyan halálos, mint napi 15 cigaretta.
{{/if}}

{{if _.parasite}}
b: A bulikban úgyis csak folyron aggódunk, hogy inkább dolgoznunk kellene.
{{/if}}

{{if _.whitebread}}
b: Folyton csak amiatt aggódunk, hogy az egészségtelen étel választások meg fognak ölni minket.
{{/if}}

```
bb({mouth:"normal", eyes:"normal"});
hong({mouth:"neutral", eyes:"lookaway"});
```

h: jaa, vajon miért.

`hong({eyes:"neutral"});`

`Game.OVERRIDE_TEXT_SPEED = 1.5;`

b: Szóval ha elmegyünk, rosszul fogják érezni magukat, de ha elutasítjuk a meghívást, akkor is!

`bb({body:"fear", eyes:"fear"});`

`Game.OVERRIDE_TEXT_SPEED = 1.5;`

b: MINDIG ROSSZUL ÉRZIK MAGUKAT AZ EMBEREK MIATTUNK, NEKÜNK IS ROSSZUL KÉNE

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "bad");
```

(...2500)

`hong({mouth:"anger", eyes:"anger"});`

h: Ahh. Ha így végre befogod, legyen.

h: Nem foglalkozom a meghívóval.

`_.partyinvite="ignore"`

(#act1d)

# act1d

```
bb({body:"normal", mouth:"normal", eyes:"normal"});
hong({mouth:"neutral", eyes:"annoyed"});
```

h: Egyébként is. A Facebook kicsit sok most. Valami nyugodtabb, kevésbé szorongáskeltő kell.

`hong({eyes:"neutral"});`

h: Mi újság Twitter-en?

`bb({eyes:"look"});`

[Jaj, ne, nézd azt a borzasztó újságcikket!](#act1d_news)

[Jaj, ne, az a tweet titokban *rólunk* szól?](#act1d_subtweet)

[Hé, egy GIF egy tejet ivó cicáról](#act1d_milk)


# act1d_news

```
bb({eyes:"pained1"});
music(null, {fade:2});
```

b: Istenem, olyan, mint ha égne a világ, nem igaz?

```
bb({eyes:"pained2"});
hong({mouth:"sad", eyes:"sad"});
```

b: Mint ha mindennek vége lenne, mint ha minden haldokolna, halálra lennénk ítélve, és semmit nem tehetünk ellene.

```
Game.OVERRIDE_TEXT_SPEED = 0.5;
bb({mouth:"shut"});
```

b: ...

`bb({mouth:"smile", eyes:"smile"});`

b: Retweet-eljük ezt a sztorit!

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

h: Jó, retweet-elem, csak kérlek maradj csendben!

`hong({mouth:"neutral", eyes:"annoyed"});`

h: Francba vele, nézzük a Snapchat-et.

(#act1e)


# act1d_subtweet

`bb({eyes:"fear"});`

b: Ez egy subtweet! Egy alattomos, bujkáló subtweet!

`hong({eyes:"annoyed"});`

h: Valószínűleg nem?

`bb({eyes:"narrow", mouth:"small"});`

b: de mi van, ha mind a hátunk mögött beszélnek

h: De n--

`bb({body:"fear", eyes:"fear", mouth:"normal"});`

b: A HÁTUNK ELŐTT

`hong({eyes:"sad", mouth:"sad"});`

h: Nem h--

`bb({eyes:"narrow", mouth:"small"});`

b: de *mi van akkor*

h: N--

`bb({eyes:"narrow_eyebrow"});`

b: *mi van akkor*

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

h: o-KÉ, megpróbálom a Snapchat-et.

(#act1e)

# act1d_milk

`hong({mouth:"smile", eyes:"neutral"});`

h: Hah, ja, ez aranyos, épp retweet-eltem, szerin--

```
hong({mouth:"shock", eyes:"shock"});
bb({body:"scream"});
Game.OVERRIDE_TEXT_SPEED = 1.8;
```

b: A MACSKÁK NEM TUDJÁK MEGEMÉSZTENI A TEJET ÉS MIND SZÖRNYŰ EMBEREK VAGYUNK, MERT ÉLVEZZÜK AZ ÁLLATKÍNZÁST

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

h: o-KÉ, megpróbálom a Snapchat-et.

(#act1e)

# act1e

`hong({mouth:"neutral", eyes:"neutral"});`

h: Hmm, tegnap esti fotók. Szóval *ilyenek* azok a heti bulik.

{{if _.partyinvite=="yes"}} (#act1e_said_yes) {{/if}}

{{if _.partyinvite=="no"}} (#act1e_said_no) {{/if}}

{{if _.partyinvite=="ignore"}} (#act1e_said_ignore) {{/if}}

# act1e_said_yes

`hong({mouth:"sad", eyes:"annoyed"});`

h: Auh, túl zsúfoltnak tűnik a szorongásomhoz.

h: Talán nem kellett volna elfogadnom a meghívást?

```
hong({mouth:"neutral", eyes:"neutral"});
bb({mouth:"normal", eyes:"normal"});
```

[Változtassunk a válaszunkon? Mint valami bunkó?!](#act1e_yes_dontchange)

[Változtassunk a válaszunkon! Túl zsúfolt!](#act1e_yes_changetono)

{{if _.subtweet}}
[Igen, tuti subtweet-eltek minket.](#act1e_ignore_subtweet)
{{/if}}

{{if _.badnews}}
[Várj, a tények ellenőrzése nélkül retweet-eltünk.](#act1e_ignore_factcheck)
{{/if}}

{{if (!_.subtweet && !_.badnews)}}
[Tudtad, hogy nagyon rossz a testtartásod?](#act1e_ignore_posture)
{{/if}}

# act1e_yes_dontchange

```
bb({eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Számítottak rá, hogy megyünk, mi meg csak így cserben hagyjuk őket? Egyedül akarsz meghalni?!

{{if _.fifteencigs}}
b: TIZENÖT. CIGARETTA.
{{/if}}

{{if _.whalepoop}}
b: BÁLNA. KAKI.
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

h: Fogd be fogd be mégis megyek!

(#act1f)

# act1e_yes_changetono

```
bb({eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Nem hallottál a tömegpánikokról?

```
bb({body:"fear", mouth:"small", eyes:"narrow"});
hong({eyes:"sad", mouth:"sad"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: 2003-ban egy Rhode Island-i klubban tűz ütött ki, az emberek pedig a pánik miatt elakadtak a kijáratoknál, így 100 ember égett halálra-

```
bb({body:"normal", mouth:"normal", eyes:"fear"});
hong({mouth:"shock"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: AZT AKAROD, HOGY VELÜNK IS EZ LEGYEN-

```
bb({body:"scream"});
Game.OVERRIDE_TEXT_SPEED = 2.5;
```

b: MONDJ NEMET MONDJ NEMET MONDJ NEMET MONDJ NEMET MONDJ N-


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

h: Fogd be fogd be nemet mondok! Jó ég!

(#act1f)

# act1e_said_no

`hong({mouth:"sad", eyes:"sad"});`

h: Hm... nagyon szórakoztatónak tűnik.

h: Lehet nem kellett volna elutasítanom a meghívást.

`bb({mouth:"normal", eyes:"normal"});`

[Változtassunk a válaszunkon? Mint valami bunkó?!](#act1e_no_dontchange)

[Változtassunk a válaszunkon! Ne haljunk meg egyedül!](#act1e_no_changetoyes)

{{if _.subtweet}}
[Igen, tuti subtweet-eltek minket.](#act1e_ignore_subtweet)
{{/if}}

{{if _.badnews}}
[Várj, a tények ellenőrzése nélkül retweet-eltünk.](#act1e_ignore_factcheck)
{{/if}}

{{if (!_.subtweet && !_.badnews)}}
[Tudtad, hogy nagyon rossz a testtartásod?](#act1e_ignore_posture)
{{/if}}

# act1e_no_dontchange

`bb({eyes:"anger"})`

b: Mindenki számított ránk!

b: ...egyedül hagyni őket egy kellemes buliban egy ilyen borzasztó, undorító{{if _.whitebread}}, fehér kenyér zabáló{{/if}} különc nélkül, mint te--


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

h: Fogd be fogd be nem megyek el!

(#act1f)

# act1e_no_changetoyes

```
bb({body:"fear", eyes:"fear", mouth:"normal"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: A krónikus magány megnöveli a kortizol szintet, a szív- és érrendszeri megbetegedések és a stroke kockázatát!

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "harm");
```

(...2500)

{{if _.fifteencigs}}
b: TIZENÖT. CIGARETTA.
{{/if}}

```
bb({body:"normal", eyes:"normal", mouth:"normal"});
hong({mouth:"anger", eyes:"anger"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

h: Fogd be fogd be mégis elmegyek! Jó ég!

(#act1f)

# act1e_ignore_subtweet

```
bb({eyes:"fear", mouth:"small"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Az összes problémás tweet-ünk visszatért kísérteni!

```
bb({body:"fear", eyes:"fear", mouth:"normal"});
Game.OVERRIDE_TEXT_SPEED = 1.7;
```

b: Ránk fognak szólni és bojkottálni fognak minket és ló mögé kötve végighúznak minket az információs szupersztrádán!

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

h: Miért vagy ilyen?!

(#act1f)

# act1e_ignore_factcheck

```
bb({eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Valótlanságot terjesztünk! Elpusztítjuk a bizalmat a szabad médiában!

```
bb({body:"scream"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Miattunk fog a demokrácia romjaiból a fasizmus felemelkedni!

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

h: Miért vagy ilyen?!

(#act1f)

# act1e_ignore_posture

```
bb({eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Szeretnél perec alakú gerincet?! Elég lesz a képernyő fölött gubbasztásból!

```
bb({body:"meta"});
```

b: És ez rád is igaz.

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

h: Miért vagy ilyen?!

(#act1f)

# act1e_said_ignore

`hong({mouth:"sad", eyes:"sad"});`

h: Hm... nagyon szórakoztatónak tűnik.

h: Lehet nem kellett volna figyelmen kívül hagyni a meghívást?

`bb({mouth:"normal", eyes:"normal"});`

[Hagyd csak, még mindig elrontjuk a bulikat.](#act1e_ignore_continue)

[Igazából mondj igent.](#act1e_ignore_changetoyes)

[Igazából mondj nemet.](#act1e_ignore_changetono)

# act1e_ignore_continue

`hong({eyes:"annoyed"});`

h: Elég szemmét dolog továbbra is figyelmen kívül hagyni őket, nem?

`bb({eyes:"normal_right"});`

b: A többiek úgyis mindig figyelmen kívül hagynak *minket*, szóval

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "alone");
```

(...2500)

`bb({eyes:"normal"});`

b: szóval azt hiszem kvittek vagyunk.

(#act1f)

# act1e_ignore_changetoyes

`hong({eyes:"surprise", mouth:"smile"});`

h: Hagyod... hogy szórakozzak?

b: Végülis, a magyányosság *képes* megölni minket.

`hong({eyes:"neutral", mouth:"neutral"});`

(#act1e_no_changetoyes)

# act1e_ignore_changetono

`bb({eyes:"narrow"});`

b: Túl zsúfolt. A tömmegek veszélyesek.

(#act1e_yes_changetono)


# act1f

```
hong({mouth:"neutral", eyes:"neutral"});
bb({body:"normal", mouth:"normal", eyes:"normal"});
```

h: Tökmindegy. Új Tinder értesítés.

`bb({eyes:"uncertain"})`

b: Mi, az az egyéjszakás kereső?

`hong({eyes:"annoyed"})`

h: Nem egyéjszakás kereső, csak lehetőség új embere--

`bb({eyes:"narrow"})`

b: Egy egyéjszakás kereső.

```
hong({eyes:"surprise", mouth:"smile"});
bb({eyes:"normal"});
```

h: Oh, lett egy találatom! Jól néz ki!

```
bb({eyes:"narrow_eyebrow"});
hong({eyes:"sad", mouth:"anger"})
```

h: Kérlek ne rontsd el ezt neke--

```
bb({body:"panic"});
Game.OVERRIDE_TEXT_SPEED = 2.0;
```

b: VESZÉLY VESZÉLY VESZÉLY VESZÉLY VESZÉLY VESZÉLY

`bb({body:"fear", eyes:"fear", mouth:"normal"})`

[A többi ember *kihasznál* minket.](#act1f_used_by_others)

[Csak *kihasználjuk* az embereket.](#act1f_using_others)

[A TALÁLATOD EGY SOROZATGYILKOS](#act1f_killer)

# act1f_used_by_others

`bb({body:"point_crotch", eyes:"normal", mouth:"normal"})`

b: Az egyéjszakás kalandok betölthetik a lyukat ott lent,

b: de soha nem töltherik be a lyukat...

`bb({body:"point_heart", eyes:"pretty", mouth:"small"})`

b: *itt bent*.

(...1000)

```
bb({body:"normal", mouth:"normal", eyes:"fear"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: A lényeg, hogy EGYEDÜL FOGUNK MEGHALNI

```
hong({mouth:"shock", eyes:"shock"});
attack("18p", "alone");
```

(...2500)

`_.hookuphole=true`

(#act1g)

# act1f_using_others

`bb({eyes:"narrow", mouth:"small"})`

b: Neked más emberek nemi szervei csak gyűjteni való Pokémonok?

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

b: ♫ (Pokémon főcímdal)-

(...5600)

```
bb({mouth:"normal"});
Game.FORCE_TEXT_DURATION = 2400;
```

b: ♫ A célom, hogy ^ribanc^ legyek-

(...500)

```
bb({eyes:"narrow", mouth:"small"});
Game.FORCE_TEXT_DURATION = 2100;
```

b: ♫ Mindig más oldalán-

(...1500)

```
bb({eyes:"pretty"});
Game.FORCE_TEXT_DURATION = 2300;
```

b: ♫ Oly sok a ^fasz^, a mell, a ^segg^-

(...500)

```
bb({eyes:"fear", mouth:"normal"});
Game.FORCE_TEXT_DURATION = 2000;
```

b: ♫ de sok-sok ^szex^ vár ránk!-

(...1000)

```
bb({eyes:"smile", mouth:"smile"});
Game.FORCE_TEXT_DURATION = 1000;
```

b: ♫ LOTYÓ-MON! SZEREZD ME-

```
Game.FORCE_CANT_SKIP = false;
Game.clearText();
music(false);
bb({body:"normal", mouth:"normal", eyes:"normal"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: A lényeg, hogy manipulatív különcök vagyunk.

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
b: Foglyul ejtenek egy kútban és addig etetnek fehér kenyérrel, míg a hízás miatt a bőrödet ruhaként nem tudják hordani!
{{/if}}

{{if _.parasite}}
b: Azt mondják majd: "PRODUKTÍVABBNAK KELLETT VOLNA LENNED, TE PARAZITA", és betörik a fejed egy pomodoro órával.
{{/if}}

{{if !_.whitebread && !_.parasite}}
b: Undi konfettivé tépik a húsod, a beleidből szalagokat csinálnak, a véredet pedig bekeverik puncsnak!
{{/if}}

{{if !_.whitebread && !_.parasite}}
b: Jó lesz EZ meghívásnak?!
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

h: úgy unom már ezt a játékot.

(...700)

`Game.OVERRIDE_TEXT_SPEED = 1.5;`

h:
{{if _.fifteencigs}}"a magányosság megöl minket"... {{/if}}
{{if _.parasite}}"társadalom-paraziták vagyunk"... {{/if}}
{{if _.whitebread}}"ne edd meg azt, meg fog ölni minket"... {{/if}}
{{if _.subtweet}}"a hátunk mögött beszélnek"... {{/if}}
{{if _.badnews}}"a világ lángol"... {{/if}}
{{if _.hookuphole}}"egyedül fogunk meghalni"... {{/if}}
{{if _.serialkiller}}"ő egy sorozatgyilkos"... {{/if}}
{{if _.catmilk}}"a tej rosszat tesz a macskáknak"... {{/if}}
{{if _.pokemon}}egy ^szar^ paródia dal... {{/if}}

h: csak élni akarom az életem.

h: csak meg akarok szabdulni ettől... a fájdalomtól.

`bb({eyes:"look_sad"});`

b: Hé... ember...

`Game.OVERRIDE_TEXT_SPEED = 0.5;`

b: Minden rendben lesz.

(...600)

`bb({body:"point_heart", eyes:"look_sad_smile", mouth:"smile"});`

b: Mint hűséges védő-farkasod, mindig figyelek a veszélyekre és minden tőlem telhetőt megteszek, hogy megvédjelek.

`bb({body:"normal", eyes:"look_sad", mouth:"smile"});`

b: Megígérem.

(...600)

```
bb({body:"normal", eyes:"normal", mouth:"normal"});
hong({body:"phone1", eyes:"neutral", mouth:"neutral"});
```

h: Utolsó app. Instagram. Mid van?

`hong({eyes:"sad"});`

h: Még több... buli kép.

`hong({mouth:"sad"});`

h: Mindenki olyan boldognak tűnik. Nem aggódnak. Nem szoronganak.

`hong({mouth:"anger"});`

h: Istenem, miért nem lehetek olyan, mint ők? Miért nem lehetek egyszerűen *normális?*

`bb({eyes:"normal_right"});`

b: Ami a bulikat illeti, döntsünk a hétvégi meghívásról. Itt a végleges döntésem:

`bb({eyes:"normal"});`

[El kéne mennünk.](#act1g_go) `Game.OVERRIDE_CHOICE_LINE=true`

[Nem kéne mennünk.](#act1g_dont) `Game.OVERRIDE_CHOICE_LINE=true`

# act1g_go

`_.act1g = "go"`

(#act1h)

# act1g_dont

`_.act1g = "dont"`

(#act1h)

# act1h

b: Szerint--

```
bb({eyes:"wat", mouth:"small"});
hong({body:"2_fuck"});
```

h: *^BASZD^.*

`hong({body:"2_you"});`

h: MEG.

(...500)

b: m

(...1500)

`bb({eyes:"wat_2"});`

b: mi?

`hong({body:"phone1", eyes:"anger", mouth:"anger"});`

h: IGENT fogok mondani a bulira,

{{if _.act1g=="go"}}
h: NEM azért, mert te azt szeretnéd, hanem mert *ÉN* akarom.
{{/if}}

{{if _.act1g=="dont"}}
h: Pontosan azért, MERT te nem szeretnéd.
{{/if}}

```
hong({body:"putaway"});
sfx("rustle");
```

h: NEM te irányítasz.

```
sfx("rustle2");
hong({body:"0_sammich", eyes:"0_annoyed", mouth:"0_neutral"});
```

h: És most bocsáss meg, békében meg fogom enni ezt a ^kurva^ szendvicset.

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

[ÁÁÁÁÁ MEG FOUNK HALNI](#act1h_death) `Game.OVERRIDE_CHOICE_LINE = true;`

[ÁÁÁÁÁ MINDENKI UTÁL MINKET](#act1h_loneliness) `Game.OVERRIDE_CHOICE_LINE = true;`

[ÁÁÁÁÁ BORZASZTÓ EMBEREK VAGYUNK](#act1h_worthless) `Game.OVERRIDE_CHOICE_LINE = true;`

# act1h_death

```
bb({body:"fear"});
Game.OVERRIDE_TEXT_SPEED = 3;
```

b: ÁÁÁÁÁ MEG FOGUNK HALNI ÁÁÁÁÁÁÁÁÁÁÁÁÁ

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

b: ÁÁÁÁÁ MINDENKI UTÁL MINKET ÁÁÁÁÁÁÁÁÁÁÁÁÁ

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

b: ÁÁÁÁÁ BORZASZTÓ EMBEREK VAGYUNK ÁÁÁÁÁÁÁÁÁÁÁÁÁ

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

n: GRATULÁLUNK

(...500)

n: SIKERESEN MEGVÉDTED AZ EMBERED FIZIKAI + SZOCIÁLIS + MORÁLIS IGÁNYEIT

n: NÉZDD, MILYEN HHÁLÁS ÉRTE!

(...500)

n: MOST, HOGY AZ ENERGIÁJA NULLÁN VAN, KÖZVETLENÜL BEFOLYÁSOLHATOD A CSELEKEDETEIT

`bb({mouth:"smile", eyes:"normal"});`

n: VÁLASZD KI A VÉGSŐ LÉPÉSED

`bb({mouth:"small_lock", eyes:"fear"});`

n: *VÉGEZZ VELE*

[{HARC: Büntesd meg a stresszt okozó telefont!}](#act1i_phone) `Game.OVERRIDE_CHOICE_LINE=true`

[{MENEKÜLÉS: Gömbölyödj labdává és sírj!}](#act1i_cry) `Game.OVERRIDE_CHOICE_LINE=true`

# act1i_phone

`bb({mouth:"normal", eyes:"narrow"})`

b: A telefonod pánikrohamot okoz!

`bb({eyes:"anger"})`

b: Zuckerberg és Társa átveszi az irányítást a mentális egészséged felett kapitalista pénzért!

```
bb({body:"fear", eyes:"fear"});
hong({body:"3_defeated2"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Büntesd meg a telefont! Pusztítsd el! Öld meg!

```
Game.OVERRIDE_TEXT_SPEED = 2.5;
bb({body:"flail"});
hong({body:"3_defeated3"});
_.act1_ending = "fight";
```

b: ÖLD MEG ÖLD MEG ÖLD MEG ÖLD MEG ÖLD MEG ÖLD MEG ÖLD MEG ÖLD MEG ÖLD MEG ÖLD MEG ÖLD MEG ÖLD MEG ÖLD MEG ÖLD MEG --

(#act1j)

# act1i_cry

`bb({eyes:"fear", mouth:"normal"})`

b: Az egész világ tele van veszéllyel!

```
bb({body:"fear"});
hong({body:"3_defeated2"});
Game.OVERRIDE_TEXT_SPEED = 1.5;
```

b: Tégy úgy, mint egy kis tatu! Gömbölyödj labdává a jobb védelemért!

```
Game.OVERRIDE_TEXT_SPEED = 2.5;
bb({body:"flail"});
hong({body:"3_defeated3"});
_.act1_ending = "flight";
```

b: GÖMBÖLYÖDJ ÖSSZE GÖMBÖLYÖDJ ÖSSZE GÖMBÖLYÖDJ ÖSSZE GÖMBÖLYÖDJ ÖSSZE GÖMBÖLYÖDJ ÖSSZE GÖMBÖLYÖDJ ÖSSZE -- 

(#act1j)

# act1j

`SceneSetup.act1_outro()`