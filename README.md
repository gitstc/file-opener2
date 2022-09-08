Forked from [cordova-plugin-file-opener2](https://github.com/pwlin/cordova-plugin-file-opener2)

Google Play Store Compatible
----------------------------
    
Usage
------
    cordova.plugins.fileOpener2.open(
        filePath, 
        fileMIMEType, 
        {
            error : function(){ }, 
            success : function(){ } 
        } 
    );

Examples
--------
Open a PDF document with the default PDF reader and optional callback object:

    cordova.plugins.fileOpener2.open(
        '/sdcard/Download/starwars.pdf', // You can also use a Cordova-style file uri: cdvfile://localhost/persistent/Download/starwars.pdf
        'application/pdf', 
        { 
            error : function(e) { 
                console.log('Error status: ' + e.status + ' - Error message: ' + e.message);
            },
            success : function () {
                console.log('file opened successfully'); 				
            }
        }
    );

Open a system modal to open PDF document with one of the already installed app and optional callback object:

    cordova.plugins.fileOpener2.showOpenWithDialog(
        '/sdcard/Download/starwars.pdf', // You can also use a Cordova-style file uri: cdvfile://localhost/persistent/Download/starwars.pdf
        'application/pdf', 
        { 
            error : function(e) { 
                console.log('Error status: ' + e.status + ' - Error message: ' + e.message);
            },
            success : function () {
                console.log('file opened successfully'); 				
            }
        }
    );