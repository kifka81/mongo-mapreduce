## Solución ejercicio PEOPLE

 let map = function(){emit(this.name,this.points)};
 
 let reduce = function(name,points){return Array.sum(points);};
 
 db.personas.mapReduce(map, reduce, {out:"total"});
 
{

        "result" : "total",
        
        "timeMillis" : 7730,
        
        "counts" : {
        
                "input" : 1000000,
                
                "emit" : 1000000,
                
                "reduce" : 86683,
                
                "output" : 26
                
        },
        
        "ok" : 1
        
}


db.total.find({})
