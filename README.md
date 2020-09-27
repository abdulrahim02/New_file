# New_file
Created by Abdulrahim Mulla


//New_File
#include<stdio.h>
#include<conio.h>
main()
{
	
	/*
	Creating the New File		:	fopen with attributes "a" or "a+" or "w" or "w+"
	Opening the Existing File	:	fopen
	Reading from the File		:	fscanf or fgetc
	Writing to the File			:	fprintf or puts
	Moving location in File		:	fseek or rewind
	Closing the File			:	fclose
	*/
	
	//Declare the File Pointer
	FILE *fp;
	char name[20];
	char username[15];
	int age;
	
	//OPEN - Read, Write and Append
	fp = fopen("newfile.txt","w");
	
	//READ content from file
	if(fp==NULL)
	{
		printf("File is Invalid");	
	}
	
	//WRITING the File
	printf("Enter the name : ");
	scanf("%s", name);
	fprintf(fp, "Name is %s \n ",name);
	
	printf("Enter the age : ");
	scanf("%d", &age);	
	fprintf(fp,"Age is %d ",age);
	
	printf("Enter the Username : ");
	scanf("%s", username);
	fprintf(fp,"Username is %s \n",username);

	//LOCATION to File
	

	//CLOSING the File
	fclose(fp);
}
