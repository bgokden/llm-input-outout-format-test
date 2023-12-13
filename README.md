# llm-input-outout-format-test
A repo to test input and output format for LLMs

This is a test if Human formatted input and outputs are faster, easier for LLMs to process.
Following results are mostly inconclisive since they are very close. 
Test should be repeated with larger iterations.

```
pyenv shell 3.10.9
python -m venv .venv
pip install langchain openai python-dotenv
```

Create a .env file with `OPENAI_API_KEY` set.


```
python main_human.py
Result for Key 'FastTiger': {'success': True, 'duration': 1.1943368911743164, 'calculated_sum': 214, 'expected_sum': 214}
Result for Key 'FastLaptop': {'success': True, 'duration': 2.0679399967193604, 'calculated_sum': 319, 'expected_sum': 319}
Result for Key 'FastCar': {'success': True, 'duration': 1.5662341117858887, 'calculated_sum': 398, 'expected_sum': 398}
Result for Key 'FastTree': {'success': True, 'duration': 1.5480310916900635, 'calculated_sum': 283, 'expected_sum': 283}
Result for Key 'FastBook': {'success': True, 'duration': 1.7554802894592285, 'calculated_sum': 148, 'expected_sum': 148}
Result for Key 'BrightTiger': {'success': True, 'duration': 1.9579710960388184, 'calculated_sum': 205, 'expected_sum': 205}
Result for Key 'BrightLaptop': {'success': True, 'duration': 1.5524260997772217, 'calculated_sum': 313, 'expected_sum': 313}
Result for Key 'BrightCar': {'success': True, 'duration': 1.1771390438079834, 'calculated_sum': 285, 'expected_sum': 285}
Result for Key 'BrightTree': {'success': True, 'duration': 0.8977160453796387, 'calculated_sum': 280, 'expected_sum': 280}
Result for Key 'BrightBook': {'success': True, 'duration': 1.5518872737884521, 'calculated_sum': 165, 'expected_sum': 165}
Result for Key 'ShinyTiger': {'success': True, 'duration': 1.3532109260559082, 'calculated_sum': 156, 'expected_sum': 156}
Result for Key 'ShinyLaptop': {'success': True, 'duration': 1.1713721752166748, 'calculated_sum': 278, 'expected_sum': 278}
Result for Key 'ShinyCar': {'success': True, 'duration': 1.3414251804351807, 'calculated_sum': 322, 'expected_sum': 322}
Result for Key 'ShinyTree': {'success': True, 'duration': 2.7448298931121826, 'calculated_sum': 234, 'expected_sum': 234}
Result for Key 'ShinyBook': {'success': True, 'duration': 1.541778802871704, 'calculated_sum': 373, 'expected_sum': 373}
Result for Key 'SharpTiger': {'success': True, 'duration': 0.7828528881072998, 'calculated_sum': 217, 'expected_sum': 217}
Result for Key 'SharpLaptop': {'success': True, 'duration': 2.2541019916534424, 'calculated_sum': 282, 'expected_sum': 282}
Result for Key 'SharpCar': {'success': True, 'duration': 1.1687750816345215, 'calculated_sum': 274, 'expected_sum': 274}
Result for Key 'SharpTree': {'success': True, 'duration': 1.2111830711364746, 'calculated_sum': 347, 'expected_sum': 347}
Result for Key 'SharpBook': {'success': True, 'duration': 0.7005960941314697, 'calculated_sum': 342, 'expected_sum': 342}
Result for Key 'SmartTiger': {'success': True, 'duration': 0.9334232807159424, 'calculated_sum': 268, 'expected_sum': 268}
Result for Key 'SmartLaptop': {'success': True, 'duration': 1.2219350337982178, 'calculated_sum': 221, 'expected_sum': 221}
Result for Key 'SmartCar': {'success': True, 'duration': 1.4665160179138184, 'calculated_sum': 214, 'expected_sum': 214}
Result for Key 'SmartTree': {'success': True, 'duration': 1.3447949886322021, 'calculated_sum': 278, 'expected_sum': 278}
Result for Key 'SmartBook': {'success': True, 'duration': 1.14984130859375, 'calculated_sum': 237, 'expected_sum': 237}
Average Duration: 1.4262319469451905 seconds
Average Relative Mean Error: 0.0%
```

```
python main_json.py 
Result for Key 'FastTiger': {'success': True, 'duration': 1.4322378635406494, 'calculated_sum': 214, 'expected_sum': 214}
Result for Key 'FastLaptop': {'success': True, 'duration': 1.4327359199523926, 'calculated_sum': 319, 'expected_sum': 319}
Result for Key 'FastCar': {'success': True, 'duration': 1.4730019569396973, 'calculated_sum': 398, 'expected_sum': 398}
Result for Key 'FastTree': {'success': True, 'duration': 0.9797301292419434, 'calculated_sum': 283, 'expected_sum': 283}
Result for Key 'FastBook': {'success': True, 'duration': 1.1253950595855713, 'calculated_sum': 148, 'expected_sum': 148}
Result for Key 'BrightTiger': {'success': True, 'duration': 1.6313700675964355, 'calculated_sum': 205, 'expected_sum': 205}
Result for Key 'BrightLaptop': {'success': True, 'duration': 1.5471138954162598, 'calculated_sum': 313, 'expected_sum': 313}
Result for Key 'BrightCar': {'success': True, 'duration': 1.760115146636963, 'calculated_sum': 285, 'expected_sum': 285}
Result for Key 'BrightTree': {'success': True, 'duration': 1.5506138801574707, 'calculated_sum': 280, 'expected_sum': 280}
Result for Key 'BrightBook': {'success': True, 'duration': 0.9373040199279785, 'calculated_sum': 165, 'expected_sum': 165}
Result for Key 'ShinyTiger': {'success': True, 'duration': 0.8601269721984863, 'calculated_sum': 156, 'expected_sum': 156}
Result for Key 'ShinyLaptop': {'success': True, 'duration': 1.6288321018218994, 'calculated_sum': 278, 'expected_sum': 278}
Result for Key 'ShinyCar': {'success': True, 'duration': 1.549591064453125, 'calculated_sum': 322, 'expected_sum': 322}
Result for Key 'ShinyTree': {'success': True, 'duration': 1.13624906539917, 'calculated_sum': 234, 'expected_sum': 234}
Result for Key 'ShinyBook': {'success': True, 'duration': 2.1670591831207275, 'calculated_sum': 373, 'expected_sum': 373}
Result for Key 'SharpTiger': {'success': True, 'duration': 2.166351079940796, 'calculated_sum': 217, 'expected_sum': 217}
Result for Key 'SharpLaptop': {'success': True, 'duration': 1.9469881057739258, 'calculated_sum': 282, 'expected_sum': 282}
Result for Key 'SharpCar': {'success': True, 'duration': 1.5598559379577637, 'calculated_sum': 274, 'expected_sum': 274}
Result for Key 'SharpTree': {'success': True, 'duration': 1.3624699115753174, 'calculated_sum': 347, 'expected_sum': 347}
Result for Key 'SharpBook': {'success': True, 'duration': 1.737272024154663, 'calculated_sum': 342, 'expected_sum': 342}
Result for Key 'SmartTiger': {'success': True, 'duration': 1.3476181030273438, 'calculated_sum': 268, 'expected_sum': 268}
Result for Key 'SmartLaptop': {'success': True, 'duration': 2.3711161613464355, 'calculated_sum': 221, 'expected_sum': 221}
Result for Key 'SmartCar': {'success': True, 'duration': 1.1405789852142334, 'calculated_sum': 214, 'expected_sum': 214}
Result for Key 'SmartTree': {'success': True, 'duration': 1.2428030967712402, 'calculated_sum': 278, 'expected_sum': 278}
Result for Key 'SmartBook': {'success': True, 'duration': 1.0670788288116455, 'calculated_sum': 237, 'expected_sum': 237}
Average Duration: 1.4861443424224854 seconds
Average Relative Mean Error: 0.0%
```