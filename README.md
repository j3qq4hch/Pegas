# Материнская плата БПЛА Pegas

Данный репозиторий содержит документацию и исходные файлы печатных плат электроники БПЛА Пегас.
Набортная электроника представляет собой главным образом материнскую плату (одну или набор из двух), которая служит для распределения питания внутри дрона, а также предоставляет интерфейс для подключения внешних устройств к автопилоту (удобные в производстве и использовании разъемы в удобных местах). БПЛА Пегас использует PX4-совместимый автопилот Cube Orange, которому всегда требуется некая материнская плата (carrier board в репозитории самого автопилота), т.к. он подключается ко всем внешним устройствам разъемом Hirose DF17(1.0H)-80DP-0.5V(57).

Было спроектировано несколько итераций электроники БПЛА Пегас.
## V1 
Самая первая версия устройства, состоящая из одной четырехслойной печатной платы.
Было произведен только один прототип, после чего была спроектирована следующая версия.

## V2
Минимальные отличия от V1, в частности: иная ориентация Cube Orange на плате (он повернут на 60 градусов), что было вызвано багом с устновлением нулевого положения встроенного компаса в ПО PX4, также добавлена схема выключения устройства на N-канальных полевых транзисторах. Схема выключения в этой версии неработоспособна и никогда не была исправлена. 

Также эта версия может быть дополнена внешним ethernet-роутером, который монтируется внутри фюзеляжа БПЛА на специальном кронштейне.

Было спроектировано две платы переходника для покупных модулей роутеров:

Было произведено несколько плат (до 10), которые используются в первых коммерческих аппаратах.

## V3
Полностью переработанная версия электроники: одна четырехслойная материнская плата  заменена на две двухслойные, соединенные мезонинным способом. Снизу располагается силовая плата, на которой размещаются разъемы для подключения моторов, медные полигоны распреления силового питания, DC-DC преобразователи всех вторичных линий питания, а также схема выключения на N-канальных полевых транзисторах. Сверху располагается плата логики с автопилотом и всеми разъемами для подключения внешних устройств. В этой версии произошел переход с миниатюрных разъемов серии JST-GH (как в UAVCAN) на несколько более крупные и значительно более удобные и надежные разъемы JST-XA с защелкой. 

Этот вариант материнской платы предназначен для сборки СЫЧ-версии Пегаса, поэтому помимо типичных компонентов на плате логики также располагается располагается покупной модуль ethernet-концентратора (ссылка тут) и модем телеметрии, поставляемый заказчиком (картинка тут).

Эта версия электроники никогда не была произведена и послужила основой для версии 3.1.

## V3.1
