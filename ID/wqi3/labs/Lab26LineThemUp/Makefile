# FILE_NAME represents the solution file name found in ./soln (without the .cpp header)
FILE_NAME=line
CLEAN=$(MAKE) -s clean

run: build
	./build/$(FILE_NAME)
	$(CLEAN)

tests: build
	chmod u+x ../../tests/app.js
	node ../../tests/app.js "./tests" "./build/$(FILE_NAME)"
	$(CLEAN)

build:
	mkdir -p build
	g++ ./soln/$(FILE_NAME).cpp -o ./build/$(FILE_NAME) -Wall -std=c++11 -g
	
clean:
	rm -r ./build