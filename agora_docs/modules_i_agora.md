Personalització dels iwmodules i el Files a Àgora
=================================================
Àgora necessita implementar funcionalitats restringides al seu entorn, ja sigui per la seva estructura concreta de *multisites* o per establir restriccions en l'administració dels centres o altres *hacks*.

Per facilitar el manteniment, aquestes funcionalitats s'implementaran en els repositoris generals, però només *funcionaran* si en la configuració del *site* tenim **$ZConfig['iwmodules']['agora'] = true** i per tant, es vetllarà per a que el funcionament sigui correcte en tots els casos.

Mirarem de documenar aquí aquests *hacks* per tenir un control global senzill.

Files
-----
  - *Controller-User-checkingModule* carrega la variable de control i la reporta a les diferents funcions.
  - *Controller-User-main* cerca per Àgora informació sobre l'espai de disc de cada centre i la reporta a la plantilla *Files_user_filesList.tpl*
      - Funció *getDiskInfo* d'Àgora
      - Variable *$ZConfig['centre']['nomPropi']*

--------
