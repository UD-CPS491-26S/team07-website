# team07-website
https://ud-cps491-26s.github.io/team07-website/


plantuml code for diagrams

Data Flow:

@startuml
title Mobile App Bluetooth Light Control Flow

start

:User connects to bluetooth device;
:User selects desired color or custom;
:App Logic / Controller processes input;

if (Bluetooth connected?) then (Yes)
  :Send color command\nRed / Blue / Green / Custom;
else (No)
  :Connect Device Request;
endif


:Bluetooth Module sends signal;
:External Light Device receives command;
:Light changes color or performs custom action;
:User sees visual feedback;

stop

@enduml

Use Case:

@startuml


User --> (Open App)
User --> (Connect to Bluetooth Light)
User --> (Select Red)
User --> (Select Blue)
User --> (Select Green)
User --> (Press Custom Button)

(Connect to Bluetooth Light) --> Light
(Select Red) --> (Send Bluetooth Command)
(Select Blue) --> (Send Bluetooth Command)
(Select Green) --> (Send Bluetooth Command)
(Press Custom Button) --> (Send Custom Command)

(Send Bluetooth Command) --> Light
(Send Custom Command) --> Light
@enduml
