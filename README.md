#include <stdio.h>
#include <stdlib.h>

struct Boxes
{ /* data */
    //int unique_id;
    int length;
    int breadth;
    int height;
    //char colour[20];
    //int weight;
    struct Boxes *next;
};


struct Boxes *head; 

int main()
{
    int number_of_boxes;
    struct Boxes *box_add;
    int l,b,h;
    box_add = (struct Boxes*)malloc(sizeof(struct Boxes)); 
    head = box_add; 
    printf("Enter the number of boxes you want to add: ");
    scanf("%d", &number_of_boxes);
    for (int i = 0; i < number_of_boxes; i++)
    {
      
        printf("\nEnter Length for the box : ");
        scanf("%d", &l);
        box_add->length = l;

        printf("\nEnter Breadth for the box : ");
        scanf("%d", &b);
        box_add->breadth = b;

        printf("\nEnter Height for the box : ");
        scanf("%d", &h);
        box_add->height = h;
        
    }
    return 0;
}
