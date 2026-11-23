# voidbr-sway-config

Skel config for VoidBR SWAY Meta Package 

## VoidBR Sway Tweaks

`voidbr-sway-tweaks` (GTK4) ajusta tudo sem abrir arquivo de configuração.
Abre pelo botão 󰒓 da Waybar, pelo atalho **Super+Shift+T** ou pelo lançador de aplicativos.

| Aba | O que muda |
|---|---|
| 🪟 Janelas | Bordas (só borda / com título / sem), espessura, cor da janela em foco, espaços entre as janelas e até a tela, fonte do título, layout das áreas novas, foco segue o mouse |
| 🧱 Barra | Waybar em ilha ou inteira, opacidade, em cima / embaixo, altura e módulos |
| 🎨 Aparência | Tema GTK, modo escuro, ícones, cursor e fonte (gsettings + nwg-look + xsettingsd) |
| 🖼️ Papel de parede | Imagens do voidbr-wallpapers ou própria, e o ajuste na tela |
| ⌨️ Teclado e touchpad | Layouts, variantes, modelo ABNT2, troca de layout, Num Lock, repetição, toque, rolagem natural, velocidade |
| 🗂️ Áreas de trabalho | Quantas ficam fixas na barra, nomes (os atalhos Super+N acompanham) e o que a barra mostra |

O app não reescreve o `~/.config/sway/config`: grava os ajustes em
`~/.config/sway/config.d/90-voidbr-tweaks.conf`, lido no fim do config
(`include ~/.config/sway/config.d/*`). Antes de recarregar confere tudo com
`sway -C`; se o Sway recusar, nada é mudado. Aplica com `swaymsg reload`
(as janelas continuam abertas). **Padrão VoidBR** e **Padrão Sway** guardam
antes a configuração atual em `~/.config/voidbr/sway-tweaks-backup/`.

```sh
voidbr-sway-tweaks --aba barra      # abre direto numa aba
voidbr-sway-tweaks --padrao-voidbr  # restaura pelo terminal
```
