
VPATH = traci_testclient;utils/traci;foreign/tcpip;utils/common

all:Traci_Client.exe

Traci_Client.exe:tracitestclient_main.o TraCITestClient.o TraCIAPI.o socket.o storage.o SUMOTime.o
	g++ -o Traci_Client.exe tracitestclient_main.o TraCITestClient.o TraCIAPI.o socket.o storage.o SUMOTime.o -l ws2_32

tracitestclient_main.o:tracitestclient_main.cpp
	g++ -c $^

TraCITestClient.o:TraCITestClient.cpp
	g++ -c $^
	
TraCIAPI.o:TraCIAPI.cpp
	g++ -c $^
	
socket.o:socket.cpp
	g++ -c $^
	
storage.o:storage.cpp
	g++ -c $^
	
SUMOTime.o:SUMOTime.cpp
	g++ -c $^

clean:
	del Traci_Client.exe tracitestclient_main.o TraCITestClient.o socket.o storage.o SUMOTime.o TraCIAPI.o