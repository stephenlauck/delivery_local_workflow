# delivery_local_workflow
## demonstrate how to do local development using the delivery-cli and test-kitchen

### setup your repo with a build cookbook and run the delivery-cli locally and via test-kitchen
```
chef generate cookbook delivery_local_workflow
cd delivery_local_workflow
git add .
git commit -m 'initial commit of delivery_local_workflow'
delivery init --local
delivery job verify "unit lint syntax" --local
cd .delivery/build-cookbook
kitchen list
kitchen converge default-centos-71
```
