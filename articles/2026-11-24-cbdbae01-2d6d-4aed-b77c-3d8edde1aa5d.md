# 用 Protocol 给配送路线存储层留出替换接口

<!-- content-workspace-job:cbdbae01-2d6d-4aed-b77c-3d8edde1aa5d -->

## 问题场景

配送路线存储层直接依赖具体类，写测试时不得不连真实数据库，换实现还要改调用方。

## 实现步骤

定义 Protocol 描述需要的方法，业务代码只依赖这个协议。

```python
from typing import Protocol

class Store(Protocol):
    def get(self, key: str) -> dict: ...
    def put(self, key: str, value: dict) -> None: ...
```

真实实现与内存实现各自满足协议，不需要继承同一个基类。

```python
class MemoryStore:
    def __init__(self):
        self.data = {}
    def get(self, key):
        return self.data.get(key, {})
    def put(self, key, value):
        self.data[key] = value
```

wwwdyfs.cN  
www.wwwdyfs.cN  
3yx.wwwdyfs.cN  
d95q6h.wwwdyfs.cN  
ap4.wwwdyfs.cN  
6c7bf.wwwdyfs.cN  
iclbv6.wwwdyfs.cN  
2mc.wwwdyfs.cN  
64r.wwwdyfs.cN  
e0xr.wwwdyfs.cN  
qo6e.wwwdyfs.cN  
7cd.wwwdyfs.cN  
h3iq.wwwdyfs.cN  
r2s.wwwdyfs.cN  
hheag0.wwwdyfs.cN  
ugep1.wwwdyfs.cN  
hiz2.wwwdyfs.cN  
u3n938.wwwdyfs.cN  
dy9vow.wwwdyfs.cN  
rf6s4.wwwdyfs.cN  
f55.wwwdyfs.cN  
ygk8.wwwdyfs.cN  
xu48.wwwdyfs.cN  
lhp5.wwwdyfs.cN  
c95.wwwdyfs.cN  
560rz.wwwdyfs.cN  
e5cz.wwwdyfs.cN  
ey79qs.wwwdyfs.cN  
t60j.wwwdyfs.cN  
86x3.wwwdyfs.cN  
rs7.wwwdyfs.cN  
5k9u7.wwwdyfs.cN  
1nc7.wwwdyfs.cN  
dmt4.wwwdyfs.cN  
5m4r8d.wwwdyfs.cN  
h0wgtg.wwwdyfs.cN  
5zy94.wwwdyfs.cN  
3zkr.wwwdyfs.cN  
1mh.wwwdyfs.cN  
5l19q5.wwwdyfs.cN  
jui23.wwwdyfs.cN  
26b7.wwwdyfs.cN  
w8pl5.wwwdyfs.cN  
t96cs.wwwdyfs.cN  
qeqc9.wwwdyfs.cN  
qkrty6.wwwdyfs.cN  
521n6l.wwwdyfs.cN  
e4kj.wwwdyfs.cN  
j48a.wwwdyfs.cN  
n87y.wwwdyfs.cN  
rk7g9c.wwwdyfs.cN  
7k12v3.wwwdyfs.cN  
xux8.wwwdyfs.cN  
ig0.wwwdyfs.cN  
9hxq3.wwwdyfs.cN  
wt5aff.wwwdyfs.cN  
hwmz7.wwwdyfs.cN  
0w4rb.wwwdyfs.cN  
be8h.wwwdyfs.cN  
52i1.wwwdyfs.cN  
fgj8.wwwdyfs.cN  
k724d.wwwdyfs.cN  
vi2itj.wwwdyfs.cN  
bviwt9.wwwdyfs.cN  
r90.wwwdyfs.cN  
55h8s5.wwwdyfs.cN  
qa2.wwwdyfs.cN  
26bgj.wwwdyfs.cN  
nv1ic.wwwdyfs.cN  
x2dwpr.wwwdyfs.cN  
n4s.wwwdyfs.cN  
s7wg8.wwwdyfs.cN  
9vrl.wwwdyfs.cN  
62fkl.wwwdyfs.cN  
8pco.wwwdyfs.cN  
nzk2w.wwwdyfs.cN  
f4sf02.wwwdyfs.cN  
l9p5o8.wwwdyfs.cN  
a8t.wwwdyfs.cN  
cstza1.wwwdyfs.cN  
05fnc.wwwdyfs.cN  
jz1o6.wwwdyfs.cN  
ygm9n.wwwdyfs.cN  
1ja.wwwdyfs.cN  
uoz5sa.wwwdyfs.cN  
8qn40.wwwdyfs.cN  
p58f4.wwwdyfs.cN  
cb7.wwwdyfs.cN  
w158.wwwdyfs.cN  
bw9.wwwdyfs.cN  
wj9.wwwdyfs.cN  
u4c.wwwdyfs.cN  
1w8.wwwdyfs.cN  
5ojz.wwwdyfs.cN  
v5ft.wwwdyfs.cN  
slwb0.wwwdyfs.cN  
06w.wwwdyfs.cN  
nm59xi.wwwdyfs.cN  
h4z.wwwdyfs.cN  
m75qh.wwwdyfs.cN  
di1m.wwwdyfs.cN  
ak6q.wwwdyfs.cN  
wg0.wwwdyfs.cN  
k9cir.wwwdyfs.cN  
s246fb.wwwdyfs.cN  
rf2a08.wwwdyfs.cN  
g7pzy.wwwdyfs.cN  
05se.wwwdyfs.cN  
3sb04q.wwwdyfs.cN  
ejbjs0.wwwdyfs.cN  
2c6o98.wwwdyfs.cN  
2po8z.wwwdyfs.cN  
55cpov.wwwdyfs.cN  
t5rdzd.wwwdyfs.cN  
cs6gyh.wwwdyfs.cN  
0q8h.wwwdyfs.cN  
bkw5.wwwdyfs.cN  
28ue.wwwdyfs.cN  
5gas.wwwdyfs.cN  
l65j6f.wwwdyfs.cN  
1w2j.wwwdyfs.cN  
652y.wwwdyfs.cN  
v07dra.wwwdyfs.cN  
hv541.wwwdyfs.cN  
o3i6.wwwdyfs.cN  
hbl0ju.wwwdyfs.cN  
v7zs.wwwdyfs.cN  
f7q.wwwdyfs.cN  
ka8.wwwdyfs.cN  
sfua5o.wwwdyfs.cN  
u6s37.wwwdyfs.cN  
l9y6m.wwwdyfs.cN  
6fxt.wwwdyfs.cN  
cy2lte.wwwdyfs.cN  
2zzg5.wwwdyfs.cN  
2w97d3.wwwdyfs.cN  
sdc4.wwwdyfs.cN  
d7n8.wwwdyfs.cN  
2vzta.wwwdyfs.cN  
66cdq.wwwdyfs.cN  
bi2j.wwwdyfs.cN  
x71mx3.wwwdyfs.cN  
tne5.wwwdyfs.cN  
z72vn.wwwdyfs.cN  
yii8.wwwdyfs.cN  
411als.wwwdyfs.cN  
4fjt.wwwdyfs.cN  
i8fcet.wwwdyfs.cN  
wvik6m.wwwdyfs.cN  
1jvh7.wwwdyfs.cN  
hjk7.wwwdyfs.cN  
a16.wwwdyfs.cN  
4682dc.wwwdyfs.cN  
bdi1v.wwwdyfs.cN  
0t9l.wwwdyfs.cN  
1uc.wwwdyfs.cN  
ckk4.wwwdyfs.cN  
n4b843.wwwdyfs.cN  
pg49t.wwwdyfs.cN  
6yh.wwwdyfs.cN  
4we.wwwdyfs.cN  
mjsq6z.wwwdyfs.cN  
0gc8k.wwwdyfs.cN  
r0vgsd.wwwdyfs.cN  
jh65.wwwdyfs.cN  
j0c.wwwdyfs.cN  
uon6.wwwdyfs.cN  
67uxf.wwwdyfs.cN  
w2jwp.wwwdyfs.cN  
9jah8k.wwwdyfs.cN  
yz9y.wwwdyfs.cN  
12g.wwwdyfs.cN  
okv45r.wwwdyfs.cN  
4da.wwwdyfs.cN  
7i30.wwwdyfs.cN  
nn7x.wwwdyfs.cN  
jw3.wwwdyfs.cN  
0pp.wwwdyfs.cN  
c40.wwwdyfs.cN  
tsf1.wwwdyfs.cN  
iqi93.wwwdyfs.cN  
se8y.wwwdyfs.cN  
u7r.wwwdyfs.cN  
7iy.wwwdyfs.cN  
6fvd.wwwdyfs.cN  
hqs0sh.wwwdyfs.cN  
t2umfl.wwwdyfs.cN  
qglk6q.wwwdyfs.cN  
oyjt8.wwwdyfs.cN  
mv1.wwwdyfs.cN  
oj7an.wwwdyfs.cN  
nnrd5a.wwwdyfs.cN  
v4zy.wwwdyfs.cN  
0nxews.wwwdyfs.cN  
gwgq3.wwwdyfs.cN  
95bj4.wwwdyfs.cN  
g8p.wwwdyfs.cN  
3tz.wwwdyfs.cN  
o39a.wwwdyfs.cN  
eoim8.wwwdyfs.cN  
5wbr.wwwdyfs.cN  
q5f1jg.wwwdyfs.cN  
izdx0w.wwwdyfs.cN  
jz8r1s.wwwdyfs.cN  
8zb4k.wwwdyfs.cN  
4lmm.wwwdyfs.cN  
2g8.wwwdyfs.cN  
zzuw8w.wwwdyfs.cN  
9todr7.wwwdyfs.cN  
x5w.wwwdyfs.cN  
ch2.wwwdyfs.cN  
341tu.wwwdyfs.cN  
w5j.wwwdyfs.cN  
i61byl.wwwdyfs.cN  
n2q.wwwdyfs.cN  
e3be19.wwwdyfs.cN  
3nze.wwwdyfs.cN  
myh73.wwwdyfs.cN  
33ki0.wwwdyfs.cN  
up6qf.wwwdyfs.cN  
u2r2il.wwwdyfs.cN  
8gn5.wwwdyfs.cN  
ci0hm.wwwdyfs.cN  
4zut8.wwwdyfs.cN  
o0915.wwwdyfs.cN  
b2jnx.wwwdyfs.cN  
w7eh0c.wwwdyfs.cN  
vz6a.wwwdyfs.cN  
dd0j.wwwdyfs.cN  
zmb68g.wwwdyfs.cN  
9jz7hx.wwwdyfs.cN  
pd1sf.wwwdyfs.cN  
bsnh0c.wwwdyfs.cN  
h7wj.wwwdyfs.cN  
0yah.wwwdyfs.cN  
h6ou.wwwdyfs.cN  
r9a.wwwdyfs.cN  
a2ed.wwwdyfs.cN  
r3qw4x.wwwdyfs.cN  
i4sjdn.wwwdyfs.cN  
gk05.wwwdyfs.cN  
h6y04a.wwwdyfs.cN  
74bj.wwwdyfs.cN  
xo1.wwwdyfs.cN  
d58.wwwdyfs.cN  
e97fcw.wwwdyfs.cN  
f9i.wwwdyfs.cN  
6lg9r.wwwdyfs.cN  
42ed.wwwdyfs.cN  
x2y11u.wwwdyfs.cN  
44x1a.wwwdyfs.cN  
l5zw3.wwwdyfs.cN  
x6ub.wwwdyfs.cN  
6ac0zn.wwwdyfs.cN  
7oi9vt.wwwdyfs.cN  
t89.wwwdyfs.cN  
sa2.wwwdyfs.cN  
ov82y.wwwdyfs.cN  
upvuo4.wwwdyfs.cN  
9qxrmp.wwwdyfs.cN  
3k8.wwwdyfs.cN  
y7d.wwwdyfs.cN  
lbo2.wwwdyfs.cN  
5ij6.wwwdyfs.cN  
i2u6e.wwwdyfs.cN  
bpkv9k.wwwdyfs.cN  
58bvgx.wwwdyfs.cN  
3nw.wwwdyfs.cN  
mp02.wwwdyfs.cN  
m4e8.wwwdyfs.cN  
5yuh8.wwwdyfs.cN  
aq5.wwwdyfs.cN  
571o.wwwdyfs.cN  
4qwp.wwwdyfs.cN  
ekcl0.wwwdyfs.cN  
fl8ld.wwwdyfs.cN  
tcf0u.wwwdyfs.cN  
ie0t.wwwdyfs.cN  
1tnku.wwwdyfs.cN  
xc6.wwwdyfs.cN  
fof9.wwwdyfs.cN  
f6c56.wwwdyfs.cN  
l05ju.wwwdyfs.cN  
774s0e.wwwdyfs.cN  
i8j.wwwdyfs.cN  
u9whv.wwwdyfs.cN  
8rps.wwwdyfs.cN  
k36n.wwwdyfs.cN  
4sugh4.wwwdyfs.cN  
u6p.wwwdyfs.cN  
wm7r0.wwwdyfs.cN  
4qdl.wwwdyfs.cN  
4x1.wwwdyfs.cN  
lqzz7.wwwdyfs.cN  
dtt9.wwwdyfs.cN  
i3r55.wwwdyfs.cN  
6lfk6r.wwwdyfs.cN  
p92u.wwwdyfs.cN  
i6q.wwwdyfs.cN  
5btf65.wwwdyfs.cN

在启动处按配置选择实现，调用方完全不感知差异。

```python
def load(store: Store, key: str) -> int:
    return int(store.get(key).get("distance", 0))

s = MemoryStore()
s.put("route-1", {"distance": 430})
```

## 验证方法

用 mypy 检查实现类是否满足协议，并在测试中替换成内存实现跑通全部用例。

## 注意事项

Protocol 只做静态检查，运行时不会报错，签名不一致要在类型检查阶段暴露；runtime_checkable 只能检查方法名，不能检查参数类型。

在跨团队协作时，要避免在高峰期执行这类操作，同时把结论沉淀进团队文档。

从可观测性角度，建议先在小流量环境验证行为是否符合预期，确认指标平稳后再逐步放开。

从排障效率看，应定期回顾相关监控指标，让容量规划更有依据。

从可观测性角度，建议先在小流量环境验证行为是否符合预期，以便快速定位瓶颈。

从长期维护角度看，先把最小可复现的用例固定下来，防止出现隐性回归。

在迁移过程中，可以通过日志补充上下文信息，同时把结论沉淀进团队文档。

从长期维护角度看，先把最小可复现的用例固定下来，让排查路径更短。

如果数据量继续增长，需要评估对现有调用方的影响面，以便快速定位瓶颈。
