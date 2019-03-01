
https://css-tricks.com/using-multi-step-animations-transitions/


Bootstrap page design:
http://shoelace.io/ <-- for editing and styling the marvelous grid system of bootstrap

https://getbootstrap.com/docs/4.1/layout/grid/#auto-layout-columns
read all of this!

add more:
// First part of JS-File
$(document).ready(function(){

  //Error messages
  $("input").on("change", function() {
    $(this).removeClass("error");
  });
  $("input:radio[name=searchedGender]").on("change", function() {
    if (this.checked) {
      $("input:radio[name=searchedGender]").removeClass("error");
    }
  });
  $("input:radio[name=gender]").on("change", function() {
    if (this.checked) {
      $("input:radio[name=gender]").removeClass("error");
    }
  });
  $('#custom-select, .arrow').on('click',function () {
    $('.age-list').slideToggle();
    $(".arrow").toggleClass('flip');
  });
  $('.age-list li').on('click',function () {
  	$('.age-list').slideToggle();
  	$('#custom-select').text($(this).text()).toggleClass('border-green');
    $("#custom-select").val($(this).text());
    $(".arrow").toggleClass('flip');
    displayAge();
  });
});
