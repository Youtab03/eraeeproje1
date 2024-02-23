#include <stdio.h>
#include <string.h>

int main() {
    char input[100];
    char *token;
    int index = 0;

    printf("Enter a string in the format '1234,1222,yuer': ");
    fgets(input, sizeof(input), stdin);

    token = strtok(input, ",");
    while(token != NULL) {
        printf("index %d: %s\n", index, token);
        token = strtok(NULL, ",");
        index++;
    }

    return 0;
}
