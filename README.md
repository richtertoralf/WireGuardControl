# WireGuardControl

So aktivierst du das Debug-Logging in WireGuard:  
`echo 'module wireguard +p' | sudo tee /sys/kernel/debug/dynamic_debug/control`  
der gleiche Befehl mit -p kann es wieder deaktivieren:  
`echo 'module wireguard -p' | sudo tee /sys/kernel/debug/dynamic_debug/control`  
