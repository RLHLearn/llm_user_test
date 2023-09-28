# Get the parent directory name
PARENT_FOLDER_NAME := $(subst  ,,$(shell for %%I in (..) do echo %%~nxI))

.PHONY: build run watch link

build:
	docker-compose up --build

run:
	docker-compose up

watch:
	docker exec -it llm-user-test-service sh -c "cd webapp && npm run dev:watch"

link:
	docker exec -it llm-user-test-service sh -c "cd webapp && ./link_mephisto_task.sh"