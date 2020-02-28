# css 开发规范

> 使用原子类开发，基本能够完成平时css的开发，请只保持一种css开发模式

## html结构使用pug语法

## 使用原子类开发

**原子类使用说明**

- margin：m、ml、mr、mt、mb、mx、my
  - m-10 -> margin: 10px;
  - ml-10 -> margin-left: 10px;
  - mr-10 -> margin-right: 10px;
  - mb-10 -> margin-bottom: 10px;
  - mx-10 -> margin-left: 10px; margin-right: 10px;
  - my-10 -> margin-top: 10px; margin-bottom: 10px;
- padding：p、pl、pr、pt、pb、px、py
  - p-5 -> padding: 5px;
  - pl-5 -> padding-left: 5px;
  - pr-5 -> padding-right: 5px;
  - pb-5 -> padding-bottom: 5px;
  - px-5 -> padding-left: 5px; padding-right: 5px;
  - py-5 -> padding-top: 5px; padding-bottom: 5px;
- width：w、w-p
  - w-10 -> width: 10px;
  - w-p10 -> width: 10%;
- height：h、h-p
  - h-10 -> height: 10px;
  - h-p10 -> height: 10%;
- 四方向：l、r、t、b；
  - l-10 -> left: 10px;
  - r-10 -> right: 10px;
  - t-10 -> top: 10px;
  - b-10 -> bottom: 10px;
- 行高：lh
  - lh -> line-height: 10px;
- 字体：fs、fw
  - fs-10 -> font-size: 10px;
  - fw-500 -> font-weight: 500;
- border-radius：br
  - br-50 -> border-radius: 50px;

## 通用原子类

```css
/* 通用原子类 */

.vh-parent {
  position: relative;
}
.h,
.v,
.vh {
  position: absolute;
}
.v {
  top: 50%;
  transform: translateY(-50%);
}
.h,
.vh {
  left: 50%;
}
.h {
  transform: translateX(-50%);
}
.vh {
  top: 50%;
  transform: translate(-50%, -50%);
}
.bg-white {
  background-color: #fff;
}
.bg-yellow {
  background-color: #ff0;
}
.bg-blue {
  background-color: #00f;
}
.bg-green {
  background-color: green;
}
.bg-red {
  background-color: red;
}
.bg-black {
  background-color: #000;
}
.bg-ccc{
  background: #ddd;
}
.color-white {
  color: #fff;
}
.color-yellow {
  color: #ff0;
}
.color-blue {
  color: #00f;
}
.color-green {
  color: green;
}
.color-red {
  color: red;
}
.color-black {
  color: #000;
}
.text-center {
  text-align: center;
}
.text-left {
  text-align: left;
}
.text-right {
  text-align: right;
}
.dspl-inbl {
  display: inline-block;
}
.dspl-bl {
  display: block;
}
.vtal-md {
  vertical-align: middle;
}
.vtal-bt {
  vertical-align: bottom;
}
.vtal-top {
  vertical-align: top;
}
.fl-right {
  float: right;
}
.fl-left {
  float: left;
}
.bs-ct {
  box-sizing: content-box;
}
.bs-box {
  box-sizing: border-box;
}
.pst-rlt {
  position: relative;
}
.pst-absl {
  position: absolute;
}
.pst-fx {
  position: fixed;
}
.m-auto {
  margin: auto;
}
.mlr-auto {
  margin-left: auto;
  margin-right: auto;
}
.mtb-auto {
  margin-top: auto;
  margin-bottom: auto;
}
.cs-pt {
  cursor: pointer;
}
.h-scroll {
  overflow-x: scroll;
  width: 100%;
  white-space: nowrap;
  -webkit-overflow-scrolling: touch;
}
.text-ellipsis {
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}
.text-ellipsis-2{
  overflow: hidden;
  text-overflow: ellipsis;
  display: -webkit-box;
  -webkit-line-clamp: 2;
  -webkit-box-orient: vertical;
}
.text-ellipsis-3{
  overflow: hidden;
  text-overflow: ellipsis;
  display: -webkit-box;
  -webkit-line-clamp: 3;
}
.text-ellipsis-4 {
  overflow: hidden;
  text-overflow: ellipsis;
  display: -webkit-box;
  -webkit-line-clamp: 4;
}
.text-ellipsis-5{
  overflow: hidden;
  text-overflow: ellipsis;
  display: -webkit-box;
  -webkit-line-clamp: 5;
  -webkit-box-orient: vertical;
}
.word-wrap {
  white-space: pre-wrap;
  word-wrap: break-word;
  word-break: break-all;
}
/* 点击穿透 */
.event-disabled {
  pointer-events: none;
}
.ovfl-hd {
  overflow: hidden;
}
.ovfl-scroll {
  overflow: scroll;
}
.ovfl-vsb {
  overflow: visible;
}
.ovfl-x-hd {
  overflow-x: hidden;
}
.ovfl-x-scroll {
  overflow-x: scroll;
}
.ovfl-y-hd {
  overflow-y: hidden;
}
.ovfl-y-scroll {
  overflow-y: scroll;
}

.flex {
  display: flex;
}
.flex-around {
  justify-content: space-around;
}
.flex-between {
  justify-content: space-between;
}
.dspl-inbl{
  display: inline-block;
}
.dspl-block{
  display: block;
}
.m-auto{
  margin-left: auto;
  margin-right: auto;
}
.bs-bd{
  box-sizing: border-box;
}

.clear::after{
  content: '';
  display: block;
  clear: both;
}

```