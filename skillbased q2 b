import socket

def main():
  
  clientSocket = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
  clientSocket.connect(("192.168.234.128", 8080))
  
  temp_Fahrenheit = input("Please enter the temperature in Fahrenheit:")
  clientSocket.send(temp_Fahrenheit.encode())
  temp_Celcius = clientSocket.recv(1024).decode()
  print("Temperature from Fahrenheit to Celcius is:", temp_Celcius)
  
main()
 
