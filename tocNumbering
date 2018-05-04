function tocNumbering (showLevel) {
     var toc = document.getElementsByClassName ("toc");
     var level = 3; // default TOC level to show;
     var lvlOne = toc[0].children;
     var lvlOneNum = 1;
     var lvlTwoNum = 1;
     var lvlThreeNum = 1;
     var lvlFourNum = 1;
     var lvlFiveNum = 1;

     if (showLevel != 0 && showLevel != null && showLevel >=2 ) {
          level = showLevel; // making showLevel an optional variable and ensures it shows at least two levels.
     }

     // for level one headings
     for (i = 0; i<lvlOne.length; i++ && level >= 1) {
          lvlOne[i].children[0].innerHTML = lvlOneNum + "\u2003" + lvlOne[i].children[0].innerHTML;

          // for level two headings
          if (lvlOne[i].children[1] != null && level >= 2) {
               var lvlTwo = lvlOne[i].children[1].children;
               for (j = 0; j<lvlTwo.length; j++) {
                    lvlTwo[j].children[0].innerHTML = lvlOneNum + "." + lvlTwoNum + "\u2003" + lvlTwo[j].children[0].innerHTML;

                    // for level three headings
                    if (lvlTwo[j].children[1] != null) {
                         var lvlThree = lvlTwo[j].children[1].children;
                         for (k = 0; k<lvlThree.length; k++) {
                              if (level >= 3) {
                                   lvlThree[k].children[0].innerHTML = lvlOneNum + "." + lvlTwoNum + "." + lvlThreeNum + "\u2003" + lvlThree[k].children[0].innerHTML;

                                   // for level four headings
                                   if (lvlThree[k].children[1] != null) {
                                        var lvlFour = lvlThree[k].children[1].children;
                                        for (l = 0; l<lvlFour.length; l++) {
                                             if (level >= 4) {
                                                  lvlFour[l].children[0].innerHTML = lvlOneNum + "." + lvlTwoNum + "." + lvlThreeNum + "." + lvlFourNum + "\u2003" + lvlFour[l].children[0].innerHTML;

                                                  // for level five headings
                                                  if (lvlFour[l].children[1] != null) {
                                                       var lvlFive = lvlFour[l].children[1].children;
                                                       for (m = 0; m<lvlFive.length; m++) {
                                                            if (level >= 5) {
                                                                 lvlFive[m].children[0].innerHTML = lvlOneNum + "." + lvlTwoNum + "." + lvlThreeNum + "." + lvlFourNum + "." + lvlFiveNum + "\u2003" + lvlFive[m].children[0].innerHTML;
                                                                 lvlFiveNum++;
                                                            } else {
                                                                 $(lvlFive[m]).css("display","none"); // hidding level five headings
                                                            }
                                                       }
                                                       lvlFiveNum = 1;
                                                  }
                                             } else {
                                                  $(lvlFour[l]).css("display","none"); // hidding level four headings
                                             }
                                             lvlFourNum++;
                                        }
                                        lvlFourNum = 1;
                                   }
                              } else {
                                   $(lvlThree[k]).css("display","none"); // hidding level three headings
                              }
                              lvlThreeNum++;
                         }
                         lvlThreeNum = 1;
                    }
                    lvlTwoNum++;
               }
               lvlTwoNum = 1;
          }
          lvlOneNum++;
     }
}
