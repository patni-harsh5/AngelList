# AngelList
Automatic script to apply to jobs

 function apply() {
  if ($(".add-note-button > a.g-button.blue:visible").length == 0) {
    $(".browse_startups_table_row:visible").first().click();
  }
  $(".add-note-button > a.g-button.blue:visible").first().click();
  $(".interested-note:visible").first().val("I hacked AngelList to apply to jobs, and that's why you should hire me.");
  $("a.g-button.blue.interested-with-note-button:visible").first().click();
  $(".js-done").click();
  $("html, body").animate({ scrollTop: $(document).height()-$(window).height() });
  setTimeout(apply, 4000);
}
