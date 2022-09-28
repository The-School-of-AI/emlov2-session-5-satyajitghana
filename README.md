# EMLO V2 - Session 05

## Deployment on AWS Fargate

Modify `deployment.json` and modify the ip address to point to your fargate deployment public ip

so if your public ip is `65.2.48.23`

then your deployment.json will be

```json
{
	"base_url": "http://65.2.48.23/api/predict"
}
```

NOTE: DO NOT MODIFY ANY FILE OTHER THAN `deployment.json`

## Running Tests

```bash
python test_deploy.py
```

If your tests pass you will get output like

```text
using base_url=http://65.2.48.23/api/predict


testing: cat.png
response: {"data":[{"label":"cat","confidences":[{"label":"cat","confidence":0.999994158744812},{"label":"dog","confidence":5.6652002058399376e-6},{"label":"frog","confidence":3.1249111742681634e-8},{"label":"deer","confidence":2.6211500525619158e-8},{"label":"horse","confidence":2.0557010316224478e-8},{"label":"bird","confidence":6.691818654758208e-9},{"label":"airplane","confidence":2.7561453119773205e-9},{"label":"truck","confidence":2.4540329768285574e-9},{"label":"ship","confidence":9.43536915265497e-10},{"label":"automobile","confidence":6.190959966900778e-10}]}],"is_generating":false,"duration":0.013329029083251953,"average_duration":0.014286404564267113}
predicted label: cat
done testing: cat.png

testing: ship.png
response: {"data":[{"label":"ship","confidences":[{"label":"ship","confidence":1.0},{"label":"automobile","confidence":9.336627471157044e-9},{"label":"airplane","confidence":7.57514850846519e-9},{"label":"truck","confidence":1.1073797434590915e-9},{"label":"frog","confidence":1.0472808176231752e-9},{"label":"horse","confidence":6.553890763427717e-10},{"label":"bird","confidence":5.482366227660407e-10},{"label":"deer","confidence":3.4371433477176083e-10},{"label":"cat","confidence":2.926026088090339e-10},{"label":"dog","confidence":2.4079613303307212e-11}]}],"is_generating":false,"duration":0.013693809509277344,"average_duration":0.014259468425403942}
predicted label: ship
done testing: ship.png

testing: automobile.png
response: {"data":[{"label":"automobile","confidences":[{"label":"automobile","confidence":0.999056875705719},{"label":"cat","confidence":0.0005809720605611801},{"label":"dog","confidence":0.00027817129739560187},{"label":"ship","confidence":0.00002417233190499246},{"label":"airplane","confidence":0.00002368592868151609},{"label":"truck","confidence":0.00002277449493703898},{"label":"horse","confidence":6.169487733131973e-6},{"label":"frog","confidence":3.0082594548730412e-6},{"label":"deer","confidence":2.7477401545183966e-6},{"label":"bird","confidence":1.3877607898393762e-6}]}],"is_generating":false,"duration":0.014853715896606445,"average_duration":0.014285305271977964}
predicted label: automobile
done testing: automobile.png

testing: dog.png
response: {"data":[{"label":"dog","confidences":[{"label":"dog","confidence":1.0},{"label":"cat","confidence":9.848699633607794e-9},{"label":"ship","confidence":3.5788474406217574e-9},{"label":"automobile","confidence":7.653569444876496e-10},{"label":"horse","confidence":6.926725859557337e-10},{"label":"frog","confidence":6.077449654640077e-10},{"label":"deer","confidence":4.206467674183756e-10},{"label":"bird","confidence":3.910529955408748e-10},{"label":"airplane","confidence":2.5110252765969676e-10},{"label":"truck","confidence":1.7144097252952406e-10}]}],"is_generating":false,"duration":0.013829946517944336,"average_duration":0.014266331990559896}
predicted label: dog
done testing: dog.png

.
----------------------------------------------------------------------
Ran 1 test in 0.081s

OK
```