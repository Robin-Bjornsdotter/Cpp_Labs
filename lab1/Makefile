CXX=g++
CXXFLAGS=-g -c -Wall
SOURCES=$(wildcard *.cpp)
OBJECTS=$(SOURCES:.cpp=.o)
END_NAME=Main

all: $(OBJECTS)
	$(CXX) $(OBJECTS) -o $(END_NAME)

%.o: %.cpp
	$(CXX) $^ $(CXXFLAGS) -o $@

clean:
	rm $(OBJECTS) $(END_NAME)

run:
	./$(END_NAME)

val: $(END_NAME)
	valgrind -v ./$(END_NAME)
