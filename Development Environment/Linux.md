---
tags:
  - DevelopmentEnvironment
---
Configurando o Blue Light Filter utilizando o wlsunset 
	wlsunset -t <temp> set low temperatura (default: 4000)
	wlsunset -T <temp> set high temperature (default 6500)
	
	agora precisamos configurar o atalho para ativar e desativar para isso vamos ao ~/.config/hypr/keybindings.conf e adicionamos as seguintes linhas 
	bind = $mainMod, F9, exec, wlsunset -T 6500  
	bind = $mainMod, F10, exec, pkill wlsunset
	que define  F9 para ligar e F10 para desligar.