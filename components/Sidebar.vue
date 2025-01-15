<script setup>
function order_content_list(list) {
  // TODO: reactive?
  const res = {};
  list.forEach((e) => {
    let p = e._path.split("/").reverse();
    if (!p[0]) return;
    p.pop();
    let fa = res;
    while (p.length > 1) {
      let q = p.pop();
      if (!q) return; // Should be useless, just in case
      fa[q] ||= { title: `${q[0].toUpperCase()}${q.slice(1)}` };
      fa[q].children ||= {};
      fa = fa[q].children;
    }
    fa[p[0]] ||= {};
    Object.assign(fa[p[0]], e);
  });
  return toList(res);

  function toList(obj) {
    const res = Object.keys(obj);
    for (let i in res) {
      const item = obj[res[i]];
      if (item.children) item.children = toList(item.children);
      res[i] = obj[res[i]];
    }
    return res;
  }
}
</script>

<template>
  <ContentList path="/" v-slot="{ list }">
    <Entry :list="order_content_list(list)" />
  </ContentList>
</template>
