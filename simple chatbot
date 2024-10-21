# Project-1
#include <stdio.h>
#include <string.h>

#define MAX_INPUT 100
#define MAX_RESPONSE 100

// Pre-defined responses
char *responses[] = {
    "Hello! How can I help you today?",
    "I'm not sure I understand. Can you please rephrase?",
    "Goodbye! It was nice chatting with you.",
    "I'm sorry, I don't know the answer to that."
};

// Pre-defined commands
char *commands[] = {
    "hello",
    "hi",
    "goodbye",
    "bye",
    "help",
    "unknown"
};

int main() {
    char input[MAX_INPUT];
    int i;

    printf("Welcome to the simple chatbot! Type 'help' for available commands.\n");

    while(1) {
        printf("You: ");
        fgets(input, MAX_INPUT, stdin);
        input[strlen(input) - 1] = '\0'; // Remove newline character

        // Check for pre-defined commands
        for(i = 0; i < sizeof(commands) / sizeof(commands[0]); i++) {
            if(strcmp(input, commands[i]) == 0) {
                printf("Chatbot: %s\n", responses[i]);
                break;
            }
        }

        // If no command matches, respond with a default message
        if(i == sizeof(commands) / sizeof(commands[0])) {
            printf("Chatbot: %s\n", responses[3]);
        }
    }

    return 0;
}
