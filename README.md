# Verificador bash Linux ADN-Bash

Guia de Realització de la Pràctica: Sistema ADN-Bash
Benvinguts a la pràctica d'Ubuntu-Mate. Per garantir l'autenticitat de les vostres tasques i la integritat dels registres, utilitzarem un sistema de Blockchain de Comandes basat en hashing criptogràfic SHA-256.

### 1. Preparació de l'entorn
Abans de començar qualsevol exercici, heu d'activar el node de registre. Se us ha lliurat un fitxer binari anomenat iniciar_adn.

Passos per activar-lo:

Doneu permisos d'execució al fitxer:

Bash
```bash
chmod +x iniciar_adn
```
Executeu el binari per iniciar la sessió protegida:

Bash
```bash
./iniciar_adn
```
**Nota:** Se us obrirà una nova sub-shell. Sabreu que esteu a dins perquè apareixerà el missatge de benvinguda del sistema de traçabilitat.

### 2. Funcionament del registre (Log)
Totes les comandes que executeu a partir d'aquest moment es registraran automàticament al fitxer:
practica_<hostname>.log

Cada línia del log conté:

**Timestamp:** L'hora exacta de l'execució.  
**Comanda:** El text literal que heu escrit.  
**ID d'Integritat:** Un hash SHA-256 que encadena la comanda actual amb l'anterior.  

**[!IMPORTANT]**
NO intenteu editar el fitxer **.log** manualment. El sistema detecta qualsevol canvi en un sol caràcter, espai o l'ordre de les comandes. Si el fitxer està manipulat, la pràctica es considerarà no vàlida automàticament.

### 3. Finalització i Lliurament
Quan hagueu acabat la pràctica, simplement sortiu de la sessió protegida:

Bash
```bash
exit
```

Què heu de lliurar?

El fitxer de respostes de la pràctica (PDF/ODT).
El fitxer .log generat pel sistema.
El fitxer .log.asc (si el professor us demana signar-lo amb GPG).

### 4. Preguntes freqüents (FAQ)

P: Puc reiniciar la màquina?
R: Sí, però recorda tornar a executar ./iniciar_adn cada vegada que tornis a entrar per continuar el registre.

P: He escrit una comanda malament, la puc esborrar del log?
R: No. El log és un reflex real del teu treball. Una comanda errònia no penalitza, però manipular el log per amagar-la sí.

P: Com sé si el meu log és vàlid?
R: El professor disposa d'un verificador binari que comprova la cadena de blocs del vostre fitxer. Si la cadena es trenca, el verificador donarà error.

**Consell del Professor:** Treballeu amb naturalitat. El sistema està dissenyat per protegir el vostre esforç i demostrar que heu realitzat la feina vosaltres mateixos. Bona sort!
