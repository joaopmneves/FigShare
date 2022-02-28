# FigShare
FigShare twicked API bash sample

This is the intial script from FigShare's team. It is so simple and easy to use that I could no resist to share. Please use it at your own risk. I take no responsabilities or liabilities, you've been warned :).

The bash script needs editing so that you enter your personal token generated in FigShare's personal area (Applications bit).

Please note that you can only add one file as is although the idea is for you to twick it any way you want it.

The history behind this script is I used it to upload aroung 1 TBytes of research datasets binaries to the FigShare's King's College London tenancy. The creation of the descriptive metadata was done using another tool (SSIS).

Issues I found in inital script  were (amended):
- spliting did not allow files over 999x10Mb. (switched the for loop to 9999 10Mbyte chunks)
- filenames could not contains "'" single comas. (script uses filename input from file instead of from stdin)

To use it, copy it to a Linux machine with Curl installed.

Edit the file run_demo and add the location of the files you want to upload. Make sure the linux box you are running the script from has access to the files.
To execute run the command below:

bash run_demo
