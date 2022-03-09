<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import HeaderAll from "@/components/HeaderAll.vue";
</script>

<template class="box">
  <HeaderAll />

  <div>
    <div class="upperbox mt-2 mb-2 bg-white flex justify-center items-center">
      <div class="codearea flex justify-center items-center ">
        <textarea
          cols="55" rows="55"
          class="codearea p-5"
          type="textarea"
          placeholder="
          <script setup lang='ts'>
          import { RouterLink, RouterView } from 'vue-router'
          import HeaderAll from '@/components/HeaderAll.vue';
          </script>
          
          <template>
            <HeaderAll />
            <div class=7box bg-yellow-400'>
              <div class='upperbox bg-white flex justify-center items-center'>
                <div class='codearea flex justify-center items-center '>
                  <input class='codearea p-5' type='textarea' placeholder='hello' disabled>
                </div>
              </div>
            </div>
          </template>
          "
          disabled></textarea>
      </div>
    </div>

    <!--キーボードの設計
    - 縦五行である。
      - １４(割合: 13が同サイズ、一番右約1.6倍)
      - １４(割合: 13が同サイズ、一番ひだり約1.5倍...これは見た目の調整的に1.6ではなく1.5）
      - １３(割合: 11が同じ、残り２が1.7倍）
      - １２(割合: 10が同じ、残り２が1.8倍）
      - ５(横970pxを10等分。97px 1:2:4:2;1 => 97:194:388:194:97px)

    - 下半分の画面のサイズが338pxなのでpaddingをのぞいて330pxとする
    - 一個66pxとなる

      横が978px
        66 * 13 = 858px
        112 = 970px
        978px

      たてが338px
        - padding 8
        - 330px
      - 330 / 5 = 66px

      10
      12421
      
      以下キーボードのHTML-->

    <div class="bottombox flex justify-center items-center bg-gray-900">
      <div class="boardarea bg-gray-200 p-1">

        <!-- １行目　-->
        <div class="oneline flex">
          <div class="bg-gray-600 buttons flex justify-center items-center">
            <div class="bg-gray-100 hover:bg-indigo-400 p-2 innerbuttons">
              <div>!</div>
              <div>1</div>
            </div>
          </div>
          <div class="bg-gray-600 buttons flex justify-center items-center">
            <div class="bg-gray-100 hover:bg-indigo-400 p-2 innerbuttons">
              <div>"</div>
              <div>2</div>
            </div>
          </div>
          <div class="bg-gray-600 buttons flex justify-center items-center">
            <div class="bg-gray-100 hover:bg-indigo-400 p-2 innerbuttons">
              <div>#</div>
              <div>3</div>
            </div>
          </div>
          <div class="bg-gray-600 buttons flex justify-center items-center">
            <div class="bg-gray-100 hover:bg-indigo-400 p-2 innerbuttons"> 
              <div>$</div>
              <div>4</div>
            </div>
          </div>
          <div class="bg-gray-600 buttons flex justify-center items-center">
            <div class="bg-gray-100 hover:bg-indigo-400 p-2 innerbuttons"> 
              <div>%</div>
              <div>5</div>
            </div>
          </div>
          <div class="bg-gray-600 buttons flex justify-center items-center">
            <div class="bg-gray-100 hover:bg-indigo-400 p-2 innerbuttons"> 
              <div>&amp;</div>
              <div>6</div>
            </div>
          </div>
          <div class="bg-gray-600 buttons flex justify-center items-center">
            <div class="bg-gray-100 hover:bg-indigo-400 p-2 innerbuttons"> 
              <div>'</div>
              <div>7</div>
            </div>
          </div>
          <div class="bg-gray-600 buttons flex justify-center items-center">
            <div class="bg-gray-100 hover:bg-indigo-400 p-2 innerbuttons"> 
              <div>(</div>
              <div>8</div>
            </div>
          </div>
          <div class="bg-gray-600 buttons flex justify-center items-center">
            <div class="bg-gray-100 hover:bg-indigo-400 p-2 innerbuttons"> 
              <div>)</div>
              <div>9</div>
            </div>
          </div>
          <div class="bg-gray-600 buttons flex justify-center items-center">
            <div class="bg-gray-100 hover:bg-indigo-400 p-2 innerbuttons"> 
              <div><br/></div>
              <div>0</div>
            </div>
          </div>
          <div class="bg-gray-600 buttons flex justify-center items-center">
            <div class="bg-gray-100 hover:bg-indigo-400 p-2 innerbuttons"> 
              <div>=</div>
              <div>-</div>
            </div>
          </div>
          <div class="bg-gray-600 buttons flex justify-center items-center">
            <div class="bg-gray-100 hover:bg-indigo-400 p-2 innerbuttons"> 
              <div>^</div>
              <div>~</div>
            </div>
          </div>
          <div class="bg-gray-600 buttons flex justify-center items-center">
            <div class="bg-gray-100 hover:bg-indigo-400 p-2 innerbuttons"> 
              <div>¥</div>
              <div>|</div>
            </div>
          </div>
          <div class="bg-gray-600 onesix flex justify-center items-center">
            <div class="bg-gray-100 hover:bg-indigo-400 p-2 innerbuttons"> 
              <div><br/></div>
              <div>backspace</div>
            </div>
          </div>
        </div>

        <!-- 2行目　-->
        <div class="oneline flex">
          <div class="bg-gray-600 onefive flex justify-center items-center">
            <div class="bg-gray-100 hover:bg-indigo-400 p-2 innerbuttons"> 
              <div><br/></div>
              <div>tab</div>
            </div>
          </div>
          <div class="bg-gray-600 buttons flex justify-center items-center">
            <div class="bg-gray-100 hover:bg-indigo-400 p-2 innerbuttons"> 
              <div><br/></div>
              <div>Q</div>
            </div>
          </div>
          <div class="bg-gray-600 buttons flex justify-center items-center">
            <div class="bg-gray-100 hover:bg-indigo-400 p-2 innerbuttons"> 
              <div><br/></div>
              <div>W</div>
            </div>
          </div>
          <div class="bg-gray-600 buttons flex justify-center items-center">
            <div class="bg-gray-100 hover:bg-indigo-400 p-2 innerbuttons"> 
              <div><br/></div>
              <div>E</div>
            </div>
          </div>
          <div class="bg-gray-600 buttons flex justify-center items-center">
           <div class="bg-gray-100 hover:bg-indigo-400 p-2 innerbuttons"> 
              <div><br/></div>
              <div>R</div>
            </div>
          </div>
          <div class="bg-gray-600 buttons flex justify-center items-center">
            <div class="bg-gray-100 hover:bg-indigo-400 p-2 innerbuttons"> 
              <div><br/></div>
              <div>T</div>
            </div>
          </div>
          <div class="bg-gray-600 buttons flex justify-center items-center">
            <div class="bg-gray-100 hover:bg-indigo-400 p-2 innerbuttons"> 
              <div><br/></div>
              <div>Y</div>
            </div>
          </div>
          <div class="bg-gray-600 buttons flex justify-center items-center">
            <div class="bg-gray-100 hover:bg-indigo-400 p-2 innerbuttons"> 
              <div><br/></div>
              <div>U</div>
            </div>
          </div>
          <div class="bg-gray-600 buttons flex justify-center items-center">
            <div class="bg-gray-100 hover:bg-indigo-400 p-2 innerbuttons"> 
              <div><br/></div>
              <div>I</div>
            </div>
          </div>
          <div class="bg-gray-600 buttons flex justify-center items-center">
            <div class="bg-gray-100 hover:bg-indigo-400 p-2 innerbuttons"> 
              <div><br/></div>
              <div>O</div>
            </div>
          </div>
          <div class="bg-gray-600 buttons flex justify-center items-center">
            <div class="bg-gray-100 hover:bg-indigo-400 p-2 innerbuttons"> 
              <div><br/></div>
              <div>P</div>
            </div>
          </div>
          <div class="bg-gray-600 buttons flex justify-center items-center">
            <div class="bg-gray-100 hover:bg-indigo-400 p-2 innerbuttons"> 
              <div>`</div>
              <div>@</div>
            </div>
          </div>
          <div class="bg-gray-600 buttons flex justify-center items-center">
            <div class="bg-gray-100 hover:bg-indigo-400 p-2 innerbuttons"> 
              <div>{</div>
              <div>[</div>
            </div>
          </div>
          <div class="bg-gray-600 buttons flex justify-center items-center">
            <div class="bg-gray-100 hover:bg-indigo-400 p-2 innerbuttons"> 
              <div>}</div>
              <div>]</div>
            </div>
          </div>
        </div>

        <!-- 3行目　-->
        <div class="oneline flex">
          <div class="bg-gray-600 oneseven flex justify-center items-center">
            <div class="bg-gray-100 hover:bg-indigo-400 p-2 innerbuttons"> 
              <div><br/></div>
              <div>control</div>
            </div>
          </div>
          <div class="bg-gray-600 buttons flex justify-center items-center">
            <div class="bg-gray-100 hover:bg-indigo-400 p-2 innerbuttons"> 
              <div><br/></div>
              <div>A</div>
            </div>
          </div>
          <div class="bg-gray-600 buttons flex justify-center items-center">
            <div class="bg-gray-100 hover:bg-indigo-400 p-2 innerbuttons"> 
              <div><br/></div>
              <div>S</div>
            </div>
          </div>
          <div class="bg-gray-600 buttons flex justify-center items-center">
            <div class="bg-gray-100 hover:bg-indigo-400 p-2 innerbuttons"> 
              <div><br/></div>
              <div>D</div>
            </div>
          </div>
          <div class="bg-gray-600 buttons flex justify-center items-center">
            <div class="bg-gray-100 hover:bg-indigo-400 p-2 innerbuttons"> 
              <div><br/></div>
              <div>F</div>
            </div>
          </div>
          <div class="bg-gray-600 buttons flex justify-center items-center">
            <div class="bg-gray-100 hover:bg-indigo-400 p-2 innerbuttons"> 
              <div><br/></div>
              <div>G</div>
            </div>
          </div>
          <div class="bg-gray-600 buttons flex justify-center items-center">
            <div class="bg-gray-100 hover:bg-indigo-400 p-2 innerbuttons"> 
              <div><br/></div>
              <div>H</div>
            </div>
          </div>
          <div class="bg-gray-600 buttons flex justify-center items-center">
            <div class="bg-gray-100 hover:bg-indigo-400 p-2 innerbuttons"> 
              <div><br/></div>
              <div>J</div>
            </div>
          </div>
          <div class="bg-gray-600 buttons flex justify-center items-center">
            <div class="bg-gray-100 hover:bg-indigo-400 p-2 innerbuttons"> 
              <div><br/></div>
              <div>K</div>
            </div>
          </div>
          <div class="bg-gray-600 buttons flex justify-center items-center">
            <div class="bg-gray-100 hover:bg-indigo-400 p-2 innerbuttons"> 
              <div><br/></div>
              <div>L</div>
            </div>
          </div>
          <div class="bg-gray-600 buttons flex justify-center items-center">
            <div class="bg-gray-100 hover:bg-indigo-400 p-2 innerbuttons"> 
              <div>+</div>
              <div>;</div>
            </div>
          </div>
          <div class="bg-gray-600 buttons flex justify-center items-center">
            <div class="bg-gray-100 hover:bg-indigo-400 p-2 innerbuttons"> 
              <div>*</div>
              <div>:</div>
            </div>
          </div>
          <div class="bg-gray-600 oneseven flex justify-center items-center">
            <div class="bg-gray-100 hover:bg-indigo-400 p-2 innerbuttons"> 
              <div><br/></div>
              <div>Enter</div>
            </div>
          </div>
        </div>

        <!-- 4行目　-->
        <div class="oneline flex">
          <div class="bg-gray-600 onefive flex justify-center items-center">
            <div class="bg-gray-100 hover:bg-indigo-400 p-2 innerbuttons"> 
              <div><br/></div>
              <div>Shift</div>
            </div>
          </div>
          <div class="bg-gray-600 buttons flex justify-center items-center">
            <div class="bg-gray-100 hover:bg-indigo-400 p-2 innerbuttons"> 
              <div><br/></div>
              <div>Z</div>
            </div>
          </div>
          <div class="bg-gray-600 buttons flex justify-center items-center">
            <div class="bg-gray-100 hover:bg-indigo-400 p-2 innerbuttons"> 
              <div><br/></div>
              <div>x</div>
            </div>
          </div>
          <div class="bg-gray-600 buttons flex justify-center items-center">
            <div class="bg-gray-100 hover:bg-indigo-400 p-2 innerbuttons"> 
              <div><br/></div>
              <div>C</div>
            </div>
          </div>
          <div class="bg-gray-600 buttons flex justify-center items-center">
            <div class="bg-gray-100 hover:bg-indigo-400 p-2 innerbuttons"> 
              <div><br/></div>
              <div>V</div>
            </div>
          </div>
          <div class="bg-gray-600 buttons flex justify-center items-center">
            <div class="bg-gray-100 hover:bg-indigo-400 p-2 innerbuttons"> 
              <div><br/></div>
              <div>B</div>
            </div>
          </div>
          <div class="bg-gray-600 buttons flex justify-center items-center">
            <div class="bg-gray-100 hover:bg-indigo-400 p-2 innerbuttons"> 
              <div><br/></div>
              <div>N</div>
            </div>
          </div>
          <div class="bg-gray-600 buttons flex justify-center items-center">
            <div class="bg-gray-100 hover:bg-indigo-400 p-2 innerbuttons"> 
              <div><br/></div>
              <div>M</div>
            </div>
          </div>
          <div class="bg-gray-600 buttons flex justify-center items-center">
            <div class="bg-gray-100 hover:bg-indigo-400 p-2 innerbuttons"> 
              <div>&lt;</div>
              <div>,</div>&gt;
            </div>
          </div>
          <div class="bg-gray-600 buttons flex justify-center items-center">
            <div class="bg-gray-100 hover:bg-indigo-400 p-2 innerbuttons"> 
              <div>&gt;</div>
              <div>.</div>
            </div>
          </div>
          <div class="bg-gray-600 buttons flex justify-center items-center">
            <div class="bg-gray-100 hover:bg-indigo-400 p-2 innerbuttons"> 
              <div>?</div>
              <div>/</div>
            </div>
          </div>
          <div class="bg-gray-600 buttons flex justify-center items-center">
            <div class="bg-gray-100 hover:bg-indigo-400 p-2 innerbuttons"> 
              <div><br/></div>
              <div>_</div>
            </div>
          </div>
          <div class="bg-gray-600 oneeight flex justify-center items-center">
            <div class="bg-gray-100 hover:bg-indigo-400 p-2 innerbuttons"> 
              <div><br/></div>
              <div>Shift</div>
            </div>
          </div>
        </div>

        <!-- 5行目　-->
        <div class="oneline flex">
          <div class="bg-gray-600 onefour flex justify-center items-center">
            <div class="bg-gray-100 hover:bg-indigo-400 p-2 innerbuttons"> 
              <div><br/></div>
              <div>option</div>
            </div>
          </div>
          <div class="bg-gray-600 oneten flex justify-center items-center">
            <div class="bg-gray-100 hover:bg-indigo-400 p-2 innerbuttons"> 
              <div><br/></div>
              <div>command</div>
            </div>
          </div>
          <div class="bg-gray-600 spacebar flex justify-center items-center">
            <div class="bg-gray-100 p-2 hover:bg-indigo-400 innerbuttons"></div>
          </div>
          <div class="bg-gray-600 oneten flex justify-center items-center">
            <div class="bg-gray-100 hover:bg-indigo-400 p-2 innerbuttons"> 
              <div><br/></div>
              <div>command</div>
            </div>
          </div>
          <div class="bg-gray-600 onefour flex justify-center items-center">
            <div class="bg-gray-100 hover:bg-indigo-400 p-2 innerbuttons"> 
              <div><br/></div>
              <div></div>
            </div>
          </div>
        </div>


      </div>
    </div>
  </div>
</template>


<style>
.box{
  height: 100vh;
  width: 100%;
}
.upperbox{
  height: 45vh
}
.codearea{
  width: 70%;
  height: 100%
}
.bottombox{
  width: 100%;
  height: 45vh
}
.boardarea{
  width: 978px;
  height: 338px
}
.oneline{
  height: 66px;
  width: 100%
}
.buttons{
  width: 66px;
  height: 66px
}
.innerbuttons{
  width: 97%;
  height: 97%
}
.onefour{
  width:97px;
  height:66px
}
.onefive{
  width: 107px;
  height: 66px
}
.onesix{
  width: 112px;
  height: 66px
}
.oneseven{
  width: 122px;
  height: 66px
}
.oneeight{
  width:155px;
  height:66px
}
.oneten{
  width: 194px;
  height: 66px
}
.spacebar{
  width: 400px;
  height:66px
}
</style>
