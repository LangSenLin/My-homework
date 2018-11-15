### 1）伪代码
    1.Choose the Pattern        
    2.Press the  switch           
    3.water_in_switch(open_close)       
    4.motor_run(direction)           
    5.stop                 
    6.water_out_switch(open_close)        
    7.water_in_switch(open_close)        
    8.get_water_volume()     
    9.motor_run(direction)      
    10.stop            
    11.water_out_switch(open_close)       
    12.motor_run(direction)       
    13.stop           
    14.time_counter()        
    15.halt(returncode)           
### 2）             
	if(开始运作)            
		注水；            
	if（达到一定高度）           
		stop；            
	FOR（i=0;i<……（上限）；i++）             
		电动机转动；             
	排水         
	then           
	if（注水一定高度）         
		stop；        
	FOR（i=0;i<……（上限）；i++）        
		电动机转动；        
	stop；         
	排水；        
	FOR（i=0;i<……（上限）；i++）        
		电动机转动；
	排水；           
	halt；END   