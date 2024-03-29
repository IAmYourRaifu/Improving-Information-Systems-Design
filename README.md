# Improving-Information-Systems-Design
# Конечный автомат

Конечный автомат (FSM — Finite-state machine) это модель вычислений, основанная на гипотетической машине состояний. В один момент времени только одно состояние может быть активным. Следовательно, для выполнения каких-либо действий машина должна менять свое состояние. 

# Преимущества:

•	Могут быть легко предоставлены в виде графов, позволяя разработчикам лучше видеть различные варианты;

•	Относительно прост в написании и реализации.

# Описание

Конечный автомат состоит из таблицы переходов, текущего состояния автомата, начального и заключительного состояния. В начале программы, машина находится в начальном состоянии. При получении сигналов (триггеров), она переходит из одного состояния в другое, пока не доходит до конечного, где она более состояния не меняет. Таблица переходов показывает при каких сигналах машина переходит из одного состояния в другой. Столбцами представлены возможные сигналы, строками состояния.

![image](https://user-images.githubusercontent.com/68112443/121692315-6b34b200-cae1-11eb-9f24-5cd3aac45b49.png)

Так же конечный автомат можно представить в виде графа, где вершины — это состояния, а рёбра — это сигналы.

![image](https://user-images.githubusercontent.com/68112443/121692962-15acd500-cae2-11eb-9969-18d5cd1449ed.png)

# Примеры

ИИ строителя в видео-игре.

В виде конечного автомата можно представить искусственный интелект строителя в видео-игре. В данном случае начальным состоянием считается "Строить здание", а конечным "Ждать". Пока есть материалы для строительства, он занимается постройкой (находится в начальном состоянии). Как только материалы кончаются (сигнал "Материалы закончились"), он идёт брать их на склад, а потом возвращается (событие "Взял материалы"). Строитель переходит в состояние "Ждать" если будучи в состоянии "Строить здание" либо пришёл приказ на отмену постройки, либо если здание завершено. Так же строитель перейдёт на это состояние, если будучи в состоянии "Взять материалы на складе" произойдёт событие "Материалы закончились". 

![image](https://user-images.githubusercontent.com/68112443/121694226-5e18c280-cae3-11eb-925d-cec08fc2cedd.png)
