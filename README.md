# Vaja4-interrupt-button-STM32F0

b)Glede na vašo razvojno ploščico in razširitveno vezje s tipkami, izberite ustrezen digitalni vhod kot interrupt (GPIO_EXT…) in izhod za zeleno LED. Zapišite izbrana pina:

GPIO_EXTI0-PA0, LD3[Green Led]-PC9

d)Znotraj te funkcije zapišite ukaz za vklop/izklop zelene LED(pomagajte si z metodo toggle, glej vaja0a.)

HAL_GPIO_TogglePin(GPIOC,GPIO_PIN_9).

e)Znotraj iste funkcije dodajte še zakasnitev, ki je potrebna, ko uporabimo mehanska tipkala/stikala: for(uint32_t i=0; i<10000; i++); Koliko znaša (v mili sekundah) zapisana zakasnitev?

Zakasnitev znaša 500ms.

f)V user code begin 3 - zanka while(1) - zapišite ukaz za utripanje modre LED.

HAL_GPIO_TogglePin(GPIOC,GPIO_PIN8);.

g)V to zanko dodajte ukaz za zakasnitev z funkcijo Delay iz knjižnice HAL, in sicer pol sekunde(glej vaja0a).

HAL_Delay(500).

b)Opazujte delovanje (utripanje modre LED). Kaj se zgodi, ko pritisnemo na modro tipko na STM32F0?

Ko pa pritisnemo na modro tipko se  prižge  zelena LED.

c)Ali pritisk na modro tipko vpliva na utripanje modre LED in zakaj?

Ne vpliva na utripanje modre LED, saj je zelena LED samo interrupt za zeleno LED.

Komentar: Ko pritisnemo modro tipko na STM32F0 se prižge/ugasne zelena LED. Modra LED pa vedno utripa.

