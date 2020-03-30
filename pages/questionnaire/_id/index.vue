<template id="questionnaire">
<div class="container-fluid">
  <nav aria-label="breadcrumb">
  <ol class="breadcrumb">
    <li class="breadcrumb-item"><a href="#">Home</a></li>
    <li class="breadcrumb-item active" aria-current="page">Questionnaire</li>
  </ol>
  </nav>
  <div class="container-fluid row">
      <div class="container col-md-3" style="height: 20vh;">
        <table class="table table-borderless table-responsive-sm">
        <tbody>
          <tr>
            <td>
            <button type="button" class="btn btn-light">1</button>
            <button type="button" class="btn btn-light">2</button>
            <button type="button" class="btn btn-light">3</button>
            <button type="button" class="btn btn-light">4</button>

            </td>
          </tr>
          <tr>
            <td>
            <button type="button" class="btn btn-light">5</button>
            <button type="button" class="btn btn-light">6</button>
            <button type="button" class="btn btn-light">7</button>
            <button type="button" class="btn btn-light">8</button>

            </td>
          </tr>
          <tr>
            <td>
            <button type="button" class="btn btn-light">9</button>
            <button type="button" class="btn btn-light">10</button>
            <button type="button" class="btn btn-light">11</button>
            <button type="button" class="btn btn-light">12</button>

            </td>
          </tr>
          <tr>
            <td>
            <button type="button" class="btn btn-light">13</button>
            <button type="button" class="btn btn-light">14</button>
            <button type="button" class="btn btn-light">15</button>
            <button type="button" class="btn btn-light">16</button>

            </td>
          </tr>
          <tr>
            <td>
            <button type="button" class="btn btn-light">17</button>
            <button type="button" class="btn btn-light">18</button>
            <button type="button" class="btn btn-light">19</button>
            <button type="button" class="btn btn-light">20</button>

            </td>
          </tr>
        </tbody>
    </table>
    </div>
    <div class="container col-sm-8">
      <div id="quiz">
  
        <quiz url="~/assets/testdata.json"></quiz>
      
      </div>
    </div>
  </div>
  

</div>
</template>

<script>
import quiz from '~/components/quiz'

export default {
  components: {
      quiz
  }
}

</script>

<style>
.container-fluid{
  height: 100%;

}
</style>