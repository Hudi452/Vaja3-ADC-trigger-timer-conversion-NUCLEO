# Vaja3-ADC-trigger-timer-conversion-NUCLEO

PINOUT KONFIGURACIJA:\
![pinout](https://github.com/Hudi452/Vaja3-ADC-trigger-timer-conversion-NUCLEO/blob/main/Konfiguracija%20CubeMX.PNG)

TIMER2 KONFIGURACIJA:\
![TIM2](https://github.com/Hudi452/Vaja3-ADC-trigger-timer-conversion-NUCLEO/blob/main/TIM_konfig1.PNG)
![TIM2](https://github.com/Hudi452/Vaja3-ADC-trigger-timer-conversion-NUCLEO/blob/main/TIM_konfig2.PNG)

ADC1 KONFIGURACIJA:\
![ADC1](https://github.com/Hudi452/Vaja3-ADC-trigger-timer-conversion-NUCLEO/blob/main/ADC_konfig1.PNG)
![ADC1](https://github.com/Hudi452/Vaja3-ADC-trigger-timer-conversion-NUCLEO/blob/main/ADC_konfig2.PNG)

SLIKA VEZJA:\
![vezje](https://github.com/Hudi452/Vaja3-ADC-trigger-timer-conversion-NUCLEO/blob/main/Slika%20vezja.PNG)



ODGOVORI NA VPRAŠANJA:\
b) Pod Analog so 3 ADC pretvorniki.\
c) Naslov dodeljenega pina: PA0\
Ime izbranega kanala: IN0\
Oznaka ob dodeljenem pinu: ADC1_IN0\
f) Zelena LED je na pinu PA5\
g) Ob spremembi frekvence APB1 Timer clocks se spremeni APB1 Prescaler in HCLK frekvenca.\
j)Prescaler: 16000

KOMENTAR NA DELOVANJE:\
Prožena ADC pretvorba se izvede na vsakih 100 ms, ko časovnik prešteje do konca. Ko se ADC pretvorba konča, se zaradi ADC prekinitve nemudoma izvedejo vsi ukazi znotraj funkcije HAL_ADC_ConvCpltCallback(). Vsakič, ko se ADC pretvorba zaključi, se zaradi ukaza HAL_GPIO_TogglePin() spremeni stanje vgrajene zelene LED. Pri nalogi je prišlo do težave pri branju vrednosti spremenljivke adcVal s pomočjo Debugger, zaradi česar je bilo potrebno vrednost adcVal brati v STM Studio. 
