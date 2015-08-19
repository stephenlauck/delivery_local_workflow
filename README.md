```
chef generate cookbook delivery_local_workflow
cd delivery_local_workflow
git add .
git commit -m 'initial commit of delivery_local_workflow'
delivery init --local
delivery job verify "lint syntax unit" --local
```

```
cd delivery_local_workflow/.delivery/build-cookbook
kitchen list
kitchen converge default-centos-71
```
