# ExtractChinesseFromTextFile

1 Chose text file
2 extract only non ascii text from text file
3 export file

# Logic
 function convert(t){
            var lines = t.split('\n');
            var result = "";
            for (let i = 0; i < lines.length; i ++)
            {
               
                let lineResult = lines[i].replace(/[\x00-\x7F]/g,"");
                result += lineResult
                if (lineResult.length > 0)
                    result += '\n';
            }
            return result;
           
         
        }
