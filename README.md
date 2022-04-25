```php
<?php
  
namespace MyGithubProfile;

use DeepFocus\Studying;
use MyLife\MainGoals;
use MyLife\WorkingOn;

class AbrahaoMartins extends BackendDeveloper
{
  /**
   * @var MainGoals $mainGoals
   * @var Studying $studying
   * @var WorkingOn $workingOn
   */
  protected MainGoals $mainGoals;
  protected Studying $studying;
  protected WorkingOn $workingOn;

  /**
  * Class constructor
  *
  * @param MainGoals $mainGoals
  * @param Studying $studying
  * @param WorkingOn $workingOn
  */
  public function __construct(MainGoals $mainGoals, Studying $studying, WorkingOn $workingOn,)
  {
    $this->mainGoals = $mainGoals,
    $this->studying = $studying;
    $this->workingOn = $workingOn;
  }
  
  /**
  * I'm currently working at @wedevBr
  *
  * @return WorkingOn
  */
  public function getWorkingOnProjects(): WorkingOn
  {
    $work = $this->workingOn
      ->with('laravel', 'api_rest', 'scrum')->get('php_projects');
    
    return response()->json($work, 200);
  }
  
  /**
  * Every day studying...
  *
  * @return Studying
  */
  public function getStudyingTools(): Studying
  {
    $studying_topics = $this->studying
      ->with('php', 'laravel', 'api_rest', 'data_structure', 'solid', 'astrophysics') // why not, right?
      ->get('backend_improvement_tools');
             
    return response->json($studying_topics, 200);
  }
             
  /**
  * Future main goals
  *
  * @return MainGoals
  */
  public function getFutureMainGoals(): MainGoals
  {
    $future_goals = $this->mainGoals
      ->get('complete_senior_skill_set', 'business_skill_set', 'c-level_position');
             
    return response()->json($future_goals, 200)
  }
}

```

[//]: # (<img src="https://github.com/abrahaosrmartins/abrahaosrmartins/blob/main/carbon_vscode.png"/>)

### Everyday tools:
<div>
  <img alt="Ab-Composer" height="30" width="40" src="https://github.com/devicons/devicon/blob/master/icons/composer/composer-original.svg">
  <img alt="Ab-Laravel" height="30" width="40" src="https://github.com/devicons/devicon/blob/master/icons/laravel/laravel-plain.svg">
  <img alt="Ab-Php" height="30" width="40" src="https://github.com/devicons/devicon/blob/master/icons/php/php-plain.svg">
  <img alt="Ab-Docker" height="30" width="40" src="https://github.com/devicons/devicon/blob/master/icons/docker/docker-original.svg">
  <img alt="Ab-Vscode" height="30" width="40" src="https://github.com/devicons/devicon/blob/master/icons/vscode/vscode-original.svg">
  <img alt="Ab-Python" height="30" width="40" src="https://github.com/devicons/devicon/blob/master/icons/python/python-original.svg">
  <img alt="Ab-Trello" height="30" width="40" src="https://github.com/devicons/devicon/blob/master/icons/trello/trello-plain.svg">
  <img alt="Ab-Slack" height="30" width="40" src="https://github.com/devicons/devicon/blob/master/icons/slack/slack-original.svg">
  <img alt="Ab-Mysql" height="30" width="40" src="https://github.com/devicons/devicon/blob/master/icons/mysql/mysql-original-wordmark.svg">
</div>
  
  ##
 
<div>
  <a href = "mailto:abrahaosrmartins@gmail.com"><img src="https://img.shields.io/badge/-Gmail-%23333?style=for-the-badge&logo=gmail&logoColor=white" target="_blank"></a>
  <a href="https://www.linkedin.com/in/abrahaosrmartins/" target="_blank"><img src="https://img.shields.io/badge/-LinkedIn-%230077B5?style=for-the-badge&logo=linkedin&logoColor=white" target="_blank"></a> 
</div>
