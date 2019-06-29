# socket.py
import socket

ip = raw_input("digite o alvo: ")

for porta in range(1, 6000):
    s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
    s.settimeout(0.2)
    if s.connect_ex((ip, porta)) == 0:
         print(porta, "ABERTA")
    else:
        print(porta, "FECHADA")
