VERILATOR = verilator
VERILATOR_FLAGS = --cc --exe --build -Wall --trace

all: top_tb

top_tb: ./vsrc/top.v ./csrc/main.cpp
	$(VERILATOR) $(VERILATOR_FLAGS) ./vsrc/top.v ./csrc/main.cpp

run: top_tb
	./obj_dir/Vtop

wave: run
	gtkwave wave.vcd

clean:
	rm -rf obj_dir wave.vcd

.PHONY: all run wave clean