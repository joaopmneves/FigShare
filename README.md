# FigShare Bash example
FigShare twicked API bash sample

This is the intial script from FigShare's team. It is so simple and easy to use that I could no resist to share. Please use it at your own risk. I take no responsabilities or liabilities! You've been warned :).

The bash script needs editing so you NEED to enter your personal token generated in FigShare's personal area (Applications bit). Also, as is, it will only work with your Figshare STAGING environment and you would have to change the BASE_URL from api.figsh.com to api.figshare.com to be able to actually do some bad to your live environment.

Please note that you can only add one file per article although the idea is for you to twick it any way you want it. Please understand that you CAN ADD many files to an article with the API.

The history behind this script is I used it to upload around 1 TBytes of research datasets binaries to FigShare's King's College London tenancy. The creation of the descriptive metadata was done using another tool (SSIS - SqlServer Integration Services). 

There were some issues I found in inital script:
- spliting did not allow files over 999x10Mb (9Gbytes). (switched a for loop that splits the files to 9999x10Mbyte chunks)
- filenames could not contains "'" single quote. (script uses filename input from file instead of from stdin)

To use it, copy it to a Linux machine with Curl installed.

Edit the file run_demo and add the location of the files you want to upload. Make sure the linux box you are running the script from has access to the files. Do not forget to get your personal token from your Figshare's personal area and useit/update add_item_figsh.sh script.
Then execute the command below:

bash run_demo

After running it you should have a new article with a sugestive name and a car picture attached. 
