# nodejs


var fs = require('fs');

var lineReader = require('line-reader');

var arr=[];

//한줄씩 읽기
lineReader.eachLine('mission_01.txt', function(line, last){
   
    
    
    arr.push(line.split(" ",1));

    console.log(last);
    
    if(last){
        
        for(var i=0; i<arr.length ; i++){
            console.log(arr[i]);
        }
        
        return false; //stop reading;
    }
    
    
});

/*fs.readFile('./mission_01.txt','utf8', function(err, data){
    console.log(data);
    
    
    
});*/


console.log('프로젝트 폴더 안의 mission_01.txt 파일을 읽도록 요청');
