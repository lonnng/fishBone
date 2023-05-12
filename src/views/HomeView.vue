<template>
  <div id="chart-container"></div>
</template>

<script>
import G6 from "@antv/g6";

export default {
  data() {
    return {
      data: {
        nodes: [
          {
            id: "2021-01",
            label: "1月",
            style: {
              fill: "pink", //背景色
              stroke: "#000000", //边框
              radius: 8
            },
            labelCfg: {
              // 标签配置属性
              positions: "center", // 标签的属性，标签在元素中的位置
              style: {
                // 包裹标签样式属性的字段 style 与标签其他属性在数据结构上并行
                fontSize: 12, // 标签的样式属性，文字字体大小
                fill: "red",
                stroke: "yellow"
                // ...            // 标签的其他样式属性
              }
            }
          },
          { id: "2021-02", label: "2月" },
          { id: "2021-03", label: "3月" },
          { id: "2021-04", label: "4月" },
          { id: "2021-05", label: "5月" },
          { id: "2021-06", label: "6月" },
          { id: "2021-07", label: "7月" },
          { id: "2021-08", label: "8月" },
          { id: "2021-09", label: "9月" },
          { id: "2021-10", label: "10月" },
          { id: "2021-11", label: "11月" },
          { id: "2021-12", label: "12月" }
        ]
        // edges: [
        //   { source: '2021-01', target: '2021-02' },
        //   { source: '2021-02', target: '2021-03' },
        //   { source: '2021-03', target: '2021-04' },
        // ],
      },
      options: {
        container: "chart-container",
        width: 1800,
        height: 500,
        defaultNode: {
          type: "rect",
          labelCfg: {
            position: "center"
          },
          style: {
            fill: "#aa9f9f",
            stroke: "#f7f8f9"
          }
        },
        defaultEdge: {
          type: "polyline",
          style: {
            stroke: "#A3B1BF",
            lineWidth: 1,
            endArrow: {
              path: G6.Arrow.triangle(6, 6, 12),
              d: 12
            }
          }
        }
      }
    };
  },

  mounted() {
    const graph = new G6.Graph(this.options);
    graph.data(this.data);
    graph.render();
  }
};
</script>
