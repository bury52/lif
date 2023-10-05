# lif

```mermaid
flowchart TB
launche(Activity launche) --> Create[on Create]
Create --> Start[on Start]
Start --> Resume[on Resume]
Resume --> running(Activity running)
running --> Pause{on Pause}
Pause --> Resume
Pause --> killed(App process killed)
killed --> Create
Pause --> Stop{on Stop}
Stop --> killed
Stop --> Restart[on Restart]
Restart --> Start
Stop --> Destroy[on Destroy]
Destroy --> down(Activity shut down)
```

### Kliknięciu programowego przycisku EXIT (w oknie aplikacji):
```mermaid
flowchart TB

Pause[on Pause] --> Stop[on Stop] --> SaveInstanceState[on SaveInstanceState]

```

### Kliknięciu sprzętowego przycisku BACK (na telefonie):
```mermaid
flowchart TB

Pause[on Pause] --> Stop[on Stop] --> Destroy[on Destroy]

```

### Kliknięciu sprzętowego przycisku HOME (na telefonie)
```mermaid
flowchart TB

Pause[on Pause] --> Start[on Start] --> SaveInstanceState[on SaveInstanceState]

```

### Kliknięciu przycisku połączenia telefonicznego (CALL - zielona słuchawka)
```mermaid
flowchart TB

Pause[on Pause] --> Stop[on Stop] --> SaveInstanceState[on SaveInstanceState]

```

### Przytrzymaniu przycisku odłożenia słuchawki (HANG-UP -  czerwona słuchawka)
```mermaid
flowchart TB

Pause[on Pause] --> Stop[on Stop]

```


### Otrzymaniu tekstowej wiadomości SMS (z innego emulatora lub telefonu)

### Po otrzymaniu połączenia głosowego (z innego emulatora lub telefonu).
