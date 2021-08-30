# WireGuardControl

So aktivierst du die Fehler-Protokollierung (Debug-Logging) in WireGuard:  
`echo 'module wireguard +p' | sudo tee /sys/kernel/debug/dynamic_debug/control`  
der gleiche Befehl mit -p kann es wieder deaktivieren:  
`echo 'module wireguard -p' | sudo tee /sys/kernel/debug/dynamic_debug/control`  

Die Logs kannst du dann so aufrufen:  
`journalctl -kf`  
oder 
`dmesg -wH | grep wireguard`  
