GoCmd=go
EXE=noaa-client

default:
	@echo 'Targets:'
	@echo ' run'
	@echo ' build'
	@echo ' analyze'
	@echo ' format'
	@echo ' clean'

run: build
	@echo
	@./$(EXE)

build: $(EXE)

$(EXE): noaa-client.go lib.go util.go types_input.go types_output.go
	@$(GoCmd) build -v -o $(EXE)

analyze:
	$(GoCmd) vet

format:
	$(GoCmd) fmt

clean:
	-rm -f $(EXE)
