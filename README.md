# NetPlan
1. Установил утилиту ifconfig, вывел список сетевых интерфейсов ВМ.  
   **sudo apt install net-tools**  
   **sudo ifconfig -a**  
   **ip link show**  
   **ip -4 -o a**  
   **ip addr show**  
   **ip route show** 
   **sudo netplan try**
   <img width="1210" height="858" alt="image" src="https://raw.githubusercontent.com/MaxLepskiy/tms_hw4_network/refs/heads/main/1ifconfig.png"/>
2. Указал статический адрес для enp0s9 в файле настроек netplan. Применил изменения.  
   **sudo nano /etc/netplan/50-cloud-init.yaml**  
   **sudo netplan try**  
   <img width="1210" height="858" alt="image" src="https://raw.githubusercontent.com/MaxLepskiy/tms_hw4_network/refs/heads/main/2netplan.png"/>
3. Проверил состояние сетевого интерфейса enp0s9  
   **sudo ifconfig -a**
   <img width="1210" height="858" alt="image" src="https://raw.githubusercontent.com/MaxLepskiy/tms_hw4_network/refs/heads/main/3after.png"/>
4. Проверил настройки DNS  
   **resolvectl status**
   <img width="1210" height="858" alt="image" src="https://raw.githubusercontent.com/MaxLepskiy/tms_hw4_network/refs/heads/main/4dns.png"/>
5. Увы, далее по DNS я не понял, что от меня хотят. Для сетевых интерфейсов DNS указаны.  
# SSH
1. Установил ssh  
   **sudo apt-get install ssh**
   <img width="1210" height="858" alt="image" src="https://raw.githubusercontent.com/MaxLepskiy/tms_hw4_network/refs/heads/main/5ssh.png"/>
3. Установил OpenSSH  
   **sudo apt install openssh-server**  
4. Добавил пакет SSH-вервера в автозагрузку  
   **sudo systemctl enable ssh**  
5. Проверил работу SSH  
   **systemctl status ssh**  
6. Изменил порт ssh на 1911  
   **sudo nano /etc/ssh/ssh**  
   **systemctl restart ssh**
   <img width="1210" height="858" alt="image" src="https://raw.githubusercontent.com/MaxLepskiy/tms_hw4_network/refs/heads/main/6port.png"/>
