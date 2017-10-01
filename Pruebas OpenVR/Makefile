INC=-Iinclude -I../../openvr/headers -I/usr/include/SDL2
LIB=-L../../openvr/lib/linux64 -lopenvr_api -lGLEW -lGL -lGLU -lSDL2 -lSOIL -lglut

CSOURCE=$(wildcard src/*.cpp)
TARGETS=$(CSOURCE:src/%.cpp=build/%.o)

all: dirs build/vr

dirs:
	mkdir -p build

build/vr: $(TARGETS)
	g++ $(TARGETS) $(LIB) -o $@

build/%.o: src/%.cpp
	g++ -c $(INC) $< -o $@

.PHONY: all dirs
