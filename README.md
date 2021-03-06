# SOyA DPV Service
version 0.1.0 (10.04.2022)

Build instructions:  
* `mvn clean install`
* `java -jar target/dpv-service-0.1.0-SNAPSHOT-jar-with-dependencies.jar`


## Usage Policy Matching Service  

### Instruction:  
The service is available at   
  - local deployment: `http://localhost:2806/api/validate/usagepolicy`
  - public instance: `https://dpv.ownyourdata.eu/api/validate/usagepolicy`

Example usage: `curl -s -o /dev/null -w "%{http_code}" -H "Content-Type: application/json" -d "$(< src/test/resources/dpv/tester.json)" -X POST http://localhost:2806/api/validate/usagepolicy`  

### Input file format & response

The input file is of type `application/json` to wrap a turtle file using JSON key "usage-policy".  
There are four example turtle files in the `test/resources/dpv` directory for your references.

The output is `200` if the policy of controllers is not violating the policy of users, or `500` otherwise.

### Further Information

Find out more about the Data Privacy Vocabulary here: https://w3c.github.io/dpv/dpv/    
The current implementation was tested against v0.4 of the DPV.

## About  

Supported by the Federal Ministry for Climate Protection, Environment, Energy, Mobility, Innovation and Technology (Bundesministerium für Klimaschutz, Umwelt, Energie, Mobilität, Innovation und Technologie [BMK]) through FFG funding in the program “IKT der Zukunft” under [grant number 887052](https://projekte.ffg.at/projekt/4125456).

<img align="left" src="https://raw.githubusercontent.com/OwnYourData/dpv-service/main/res/210614_FFG-BM-Logoleisten_CMYK_01_BMDW-BMK-FFG_128mm.jpg" height="150">

<br clear="both" />

Contact `fajar.ekaputra@tuwien.ac.at` for further questions. 
