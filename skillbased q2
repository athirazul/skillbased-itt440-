import socket

def main():
    serverSocket = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
    serverSocket.bind(("192.168.234.128", 8080))
    serverSocket.listen(1)
    
    while True:
    
    clientSocket, address = serverSocket.accept()
    print("Connection established from %s"% str (address))
    
    temp_Fahrenheit = clientSocket.recv(1024).decode()
    temp_Celcius = Fahrenheit_to_Celcius(float(temp_Fahrenheit))
    temp_Celcius = round(temp_Celcius,2)
    temp_Celcius = str(temp_Celcius)
    clientSocket.send(temp_Celcius.encode())
    
def Fahrenheit_to_Celcius(temp_Fahrenheit):
    temp_Celcius = (temp_Fahrenheit - 32) * (5/9)
    return temp_Celcius
    
main()
