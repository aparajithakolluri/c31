#include <stdio.h>
#include <stdlib.h>
struct student{
    char name[50];
    int age;
    float marks;
};
int main(){
    struct student *ptr;
    ptr =(struct student*)malloc(sizeof(struct student));
    if (ptr==NULL){
        printf("memory allocation failed\n");
        return 1;
    }
    printf("Enter name:");
    scanf("%s", ptr->name);
    printf("Enter age:");
    scanf("%d", &ptr->age);
    printf("enter marks:");
    scanf("%f", &ptr->marks);
    printf("student details :\n");
    printf("Name : %s\n Age: %d \n marks:%.2f\n",ptr->name, ptr->age, ptr->marks);
    free(ptr);
    return 0;
}
