CC = arm-linux-gnueabi-gcc
# CC = arm-none-eabi-gcc

all: armforth run

armforth: armforth.S
	$(CC) -nostdlib -static -Wl,-Ttext,0 -Wl,--build-id=none -o armforth armforth.S

run:
	cat ../x86/jonesforth.f - | ./armforth

clean:
	rm -rf armforth
