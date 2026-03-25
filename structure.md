│   .dockerignore
│   .env
│   .env.development
│   .env.production
│   .gitattributes
│   .gitignore
│   .npmrc
│   docker-compose.prod.yml
│   docker-compose.yml
│   Dockerfile
│   ecosystem.config.js
│   eslint.config.mjs
│   LICENSE
│   nest-cli.json
│   package.json
│   pnpm-lock.yaml
│   README.md
│   tsconfig.build.json
│   tsconfig.json
│   vercel.json
│   wait-for-it.sh
│
├───.github
│   ├───ISSUE_TEMPLATE
│   │       bug_report.md
│   │       feature_request.md
│   │
│   └───workflows
│           build-rc.yml
│           build-stable.yml
│           daily-curl-request.yml
│           deploy.yml
│           sync-to-gitee.yml
│
├───.vscode
│       launch.json
│       settings.json
│
├───deploy
│   ├───sql
│   │       nest_admin.sql
│   │
│   └───web
│           default.conf
│
├───logs
├───scripts
│       genEnvTypes.ts
│       resetScheduler.ts
│
├───src
│   │   app.module.ts
│   │   main.ts
│   │   repl.ts
│   │   setup-swagger.ts
│   │
│   ├───assets
│   │   └───templates
│   │           verification-code-zh.hbs
│   │           verification-code.hbs
│   │
│   ├───common
│   │   ├───adapters
│   │   │       fastify.adapter.ts
│   │   │       socket.adapter.ts
│   │   │
│   │   ├───decorators
│   │   │       api-result.decorator.ts
│   │   │       bypass.decorator.ts
│   │   │       cookie.decorator.ts
│   │   │       cron-once.decorator.ts
│   │   │       field.decorator.ts
│   │   │       http.decorator.ts
│   │   │       id-param.decorator.ts
│   │   │       idempotence.decorator.ts
│   │   │       inject-redis.decorator.ts
│   │   │       swagger.decorator.ts
│   │   │       transform.decorator.ts
│   │   │
│   │   ├───dto
│   │   │       cursor.dto.ts
│   │   │       delete.dto.ts
│   │   │       id.dto.ts
│   │   │       operator.dto.ts
│   │   │       pager.dto.ts
│   │   │
│   │   ├───entity
│   │   │       common.entity.ts
│   │   │
│   │   ├───exceptions
│   │   │       biz.exception.ts
│   │   │       not-found.exception.ts
│   │   │       socket.exception.ts
│   │   │
│   │   ├───filters
│   │   │       any-exception.filter.ts
│   │   │
│   │   ├───interceptors
│   │   │       idempotence.interceptor.ts
│   │   │       logging.interceptor.ts
│   │   │       timeout.interceptor.ts
│   │   │       transform.interceptor.ts
│   │   │
│   │   ├───model
│   │   │       response.model.ts
│   │   │
│   │   └───pipes
│   │           creator.pipe.ts
│   │           parse-int.pipe.ts
│   │           updater.pipe.ts
│   │
│   ├───config
│   │       app.config.ts
│   │       database.config.ts
│   │       index.ts
│   │       mailer.config.ts
│   │       oss.config.ts
│   │       redis.config.ts
│   │       security.config.ts
│   │       swagger.config.ts
│   │
│   ├───constants
│   │       cache.constant.ts
│   │       error-code.constant.ts
│   │       event-bus.constant.ts
│   │       oss.constant.ts
│   │       response.constant.ts
│   │       system.constant.ts
│   │
│   ├───global
│   │       env.ts
│   │
│   ├───helper
│   │   │   catchError.ts
│   │   │   genRedisKey.ts
│   │   │
│   │   ├───crud
│   │   │       base.service.ts
│   │   │       crud.factory.ts
│   │   │
│   │   └───paginate
│   │           create-pagination.ts
│   │           index.ts
│   │           interface.ts
│   │           pagination.ts
│   │
│   ├───migrations
│   │       1707996695540-initData.ts
│   │       1717007831711-update-table_2_0_0.ts
│   │
│   ├───modules
│   │   ├───auth
│   │   │   │   auth.constant.ts
│   │   │   │   auth.controller.ts
│   │   │   │   auth.module.ts
│   │   │   │   auth.service.ts
│   │   │   │
│   │   │   ├───controllers
│   │   │   │       account.controller.ts
│   │   │   │       captcha.controller.ts
│   │   │   │       email.controller.ts
│   │   │   │
│   │   │   ├───decorators
│   │   │   │       allow-anon.decorator.ts
│   │   │   │       auth-user.decorator.ts
│   │   │   │       permission.decorator.ts
│   │   │   │       public.decorator.ts
│   │   │   │       resource.decorator.ts
│   │   │   │
│   │   │   ├───dto
│   │   │   │       account.dto.ts
│   │   │   │       auth.dto.ts
│   │   │   │       captcha.dto.ts
│   │   │   │
│   │   │   ├───entities
│   │   │   │       access-token.entity.ts
│   │   │   │       refresh-token.entity.ts
│   │   │   │
│   │   │   ├───guards
│   │   │   │       jwt-auth.guard.ts
│   │   │   │       local.guard.ts
│   │   │   │       rbac.guard.ts
│   │   │   │       resource.guard.ts
│   │   │   │
│   │   │   ├───models
│   │   │   │       auth.model.ts
│   │   │   │
│   │   │   ├───services
│   │   │   │       captcha.service.ts
│   │   │   │       token.service.ts
│   │   │   │
│   │   │   └───strategies
│   │   │           jwt.strategy.ts
│   │   │           local.strategy.ts
│   │   │
│   │   ├───health
│   │   │       health.controller.ts
│   │   │       health.module.ts
│   │   │
│   │   ├───netdisk
│   │   │   │   netdisk.module.ts
│   │   │   │
│   │   │   ├───manager
│   │   │   │       manage.class.ts
│   │   │   │       manage.controller.ts
│   │   │   │       manage.dto.ts
│   │   │   │       manage.service.ts
│   │   │   │
│   │   │   └───overview
│   │   │           overview.controller.ts
│   │   │           overview.dto.ts
│   │   │           overview.service.ts
│   │   │
│   │   ├───sse
│   │   │       sse.controller.ts
│   │   │       sse.module.ts
│   │   │       sse.service.ts
│   │   │
│   │   ├───system
│   │   │   │   system.module.ts
│   │   │   │
│   │   │   ├───dept
│   │   │   │       dept.controller.ts
│   │   │   │       dept.dto.ts
│   │   │   │       dept.entity.ts
│   │   │   │       dept.module.ts
│   │   │   │       dept.service.ts
│   │   │   │
│   │   │   ├───dict-item
│   │   │   │       dict-item.controller.ts
│   │   │   │       dict-item.dto.ts
│   │   │   │       dict-item.entity.ts
│   │   │   │       dict-item.module.ts
│   │   │   │       dict-item.service.ts
│   │   │   │
│   │   │   ├───dict-type
│   │   │   │       dict-type.controller.ts
│   │   │   │       dict-type.dto.ts
│   │   │   │       dict-type.entity.ts
│   │   │   │       dict-type.module.ts
│   │   │   │       dict-type.service.ts
│   │   │   │
│   │   │   ├───log
│   │   │   │   │   log.controller.ts
│   │   │   │   │   log.module.ts
│   │   │   │   │
│   │   │   │   ├───dto
│   │   │   │   │       log.dto.ts
│   │   │   │   │
│   │   │   │   ├───entities
│   │   │   │   │       captcha-log.entity.ts
│   │   │   │   │       index.ts
│   │   │   │   │       login-log.entity.ts
│   │   │   │   │       task-log.entity.ts
│   │   │   │   │
│   │   │   │   ├───models
│   │   │   │   │       log.model.ts
│   │   │   │   │
│   │   │   │   └───services
│   │   │   │           captcha-log.service.ts
│   │   │   │           login-log.service.ts
│   │   │   │           task-log.service.ts
│   │   │   │
│   │   │   ├───menu
│   │   │   │       menu.controller.ts
│   │   │   │       menu.dto.ts
│   │   │   │       menu.entity.ts
│   │   │   │       menu.model.ts
│   │   │   │       menu.module.ts
│   │   │   │       menu.service.ts
│   │   │   │
│   │   │   ├───online
│   │   │   │       online.controller.ts
│   │   │   │       online.dto.ts
│   │   │   │       online.model.ts
│   │   │   │       online.module.ts
│   │   │   │       online.service.ts
│   │   │   │
│   │   │   ├───param-config
│   │   │   │       param-config.controller.ts
│   │   │   │       param-config.dto.ts
│   │   │   │       param-config.entity.ts
│   │   │   │       param-config.module.ts
│   │   │   │       param-config.service.ts
│   │   │   │
│   │   │   ├───role
│   │   │   │       role.controller.ts
│   │   │   │       role.dto.ts
│   │   │   │       role.entity.ts
│   │   │   │       role.model.ts
│   │   │   │       role.module.ts
│   │   │   │       role.service.ts
│   │   │   │
│   │   │   ├───serve
│   │   │   │       serve.controller.ts
│   │   │   │       serve.model.ts
│   │   │   │       serve.module.ts
│   │   │   │       serve.service.ts
│   │   │   │
│   │   │   └───task
│   │   │           constant.ts
│   │   │           task.controller.ts
│   │   │           task.dto.ts
│   │   │           task.entity.ts
│   │   │           task.module.ts
│   │   │           task.processor.ts
│   │   │           task.service.ts
│   │   │           task.ts
│   │   │
│   │   ├───tasks
│   │   │   │   mission.decorator.ts
│   │   │   │   tasks.module.ts
│   │   │   │
│   │   │   └───jobs
│   │   │           email.job.ts
│   │   │           http-request.job.ts
│   │   │           log-clear.job.ts
│   │   │
│   │   ├───todo
│   │   │       todo.controller.ts
│   │   │       todo.dto.ts
│   │   │       todo.entity.ts
│   │   │       todo.module.ts
│   │   │       todo.service.ts
│   │   │
│   │   ├───tools
│   │   │   │   tools.module.ts
│   │   │   │
│   │   │   ├───email
│   │   │   │       email.controller.ts
│   │   │   │       email.dto.ts
│   │   │   │       email.module.ts
│   │   │   │
│   │   │   ├───storage
│   │   │   │       storage.controller.ts
│   │   │   │       storage.dto.ts
│   │   │   │       storage.entity.ts
│   │   │   │       storage.modal.ts
│   │   │   │       storage.module.ts
│   │   │   │       storage.service.ts
│   │   │   │
│   │   │   └───upload
│   │   │           file.constraint.ts
│   │   │           upload.controller.ts
│   │   │           upload.dto.ts
│   │   │           upload.module.ts
│   │   │           upload.service.ts
│   │   │
│   │   └───user
│   │       │   constant.ts
│   │       │   user.controller.ts
│   │       │   user.entity.ts
│   │       │   user.model.ts
│   │       │   user.module.ts
│   │       │   user.service.ts
│   │       │
│   │       └───dto
│   │               password.dto.ts
│   │               user.dto.ts
│   │
│   ├───shared
│   │   │   shared.module.ts
│   │   │
│   │   ├───database
│   │   │   │   database.module.ts
│   │   │   │   typeorm-logger.ts
│   │   │   │
│   │   │   └───constraints
│   │   │           entity-exist.constraint.ts
│   │   │           unique.constraint.ts
│   │   │
│   │   ├───helper
│   │   │       cron.service.ts
│   │   │       helper.module.ts
│   │   │       qq.service.ts
│   │   │
│   │   ├───logger
│   │   │       logger.module.ts
│   │   │       logger.service.ts
│   │   │
│   │   ├───mailer
│   │   │       mailer.module.ts
│   │   │       mailer.service.ts
│   │   │
│   │   └───redis
│   │           cache.service.ts
│   │           redis-subpub.ts
│   │           redis.constant.ts
│   │           redis.module.ts
│   │           subpub.service.ts
│   │
│   ├───socket
│   │   │   base.gateway.ts
│   │   │   business-event.constant.ts
│   │   │   socket.module.ts
│   │   │
│   │   ├───events
│   │   │       admin.gateway.ts
│   │   │       web.gateway.ts
│   │   │
│   │   └───shared
│   │           auth.gateway.ts
│   │
│   └───utils
│           captcha.util.ts
│           crypto.util.ts
│           date.util.ts
│           file.util.ts
│           index.ts
│           ip.util.ts
│           is.util.ts
│           list2tree.util.ts
│           permission.util.ts
│           redis.util.ts
│           schedule.util.ts
│           tool.util.ts
│
├───types
│       env.d.ts
│       global.d.ts
│       module.d.ts
│       utils.d.ts
│
└───__data
    └───mysql
        │   #ib_16384_0.dblwr
        │   #ib_16384_1.dblwr
        │   auto.cnf
        │   binlog.000001
        │   binlog.000002
        │   binlog.index
        │   ca-key.pem
        │   ca.pem
        │   client-cert.pem
        │   client-key.pem
        │   ibdata1
        │   ibtmp1
        │   ib_buffer_pool
        │   mysql.ibd
        │   mysql.sock
        │   mysql_upgrade_history
        │   private_key.pem
        │   public_key.pem
        │   server-cert.pem
        │   server-key.pem
        │   undo_001
        │   undo_002
        │
        ├───#innodb_redo
        │       #ib_redo10_tmp
        │       #ib_redo11_tmp
        │       #ib_redo12_tmp
        │       #ib_redo13_tmp
        │       #ib_redo14_tmp
        │       #ib_redo15_tmp
        │       #ib_redo16_tmp
        │       #ib_redo17_tmp
        │       #ib_redo18_tmp
        │       #ib_redo19_tmp
        │       #ib_redo20_tmp
        │       #ib_redo21_tmp
        │       #ib_redo22_tmp
        │       #ib_redo23_tmp
        │       #ib_redo24_tmp
        │       #ib_redo25_tmp
        │       #ib_redo26_tmp
        │       #ib_redo27_tmp
        │       #ib_redo28_tmp
        │       #ib_redo29_tmp
        │       #ib_redo30_tmp
        │       #ib_redo31_tmp
        │       #ib_redo32_tmp
        │       #ib_redo33_tmp
        │       #ib_redo34_tmp
        │       #ib_redo35_tmp
        │       #ib_redo36_tmp
        │       #ib_redo37_tmp
        │       #ib_redo38_tmp
        │       #ib_redo39_tmp
        │       #ib_redo40_tmp
        │       #ib_redo9
        │
        ├───#innodb_temp
        │       temp_1.ibt
        │       temp_10.ibt
        │       temp_2.ibt
        │       temp_3.ibt
        │       temp_4.ibt
        │       temp_5.ibt
        │       temp_6.ibt
        │       temp_7.ibt
        │       temp_8.ibt
        │       temp_9.ibt
        │
        ├───mysql
        │       general_log.CSM
        │       general_log.CSV
        │       general_log_224.sdi
        │       slow_log.CSM
        │       slow_log.CSV
        │       slow_log_225.sdi
        │
        ├───nest_admin
        │       sys_captcha_log.ibd
        │       sys_config.ibd
        │       sys_dept.ibd
        │       sys_dict.ibd
        │       sys_dict_item.ibd
        │       sys_dict_type.ibd
        │       sys_login_log.ibd
        │       sys_menu.ibd
        │       sys_role.ibd
        │       sys_role_menus.ibd
        │       sys_task.ibd
        │       sys_task_log.ibd
        │       sys_user.ibd
        │       sys_user_roles.ibd
        │       todo.ibd
        │       tool_storage.ibd
        │       user_access_tokens.ibd
        │       user_refresh_tokens.ibd
        │
        ├───performance_schema
        │       accounts_153.sdi
        │       binary_log_trans_200.sdi
        │       cond_instances_87.sdi
        │       data_locks_169.sdi
        │       data_lock_waits_170.sdi
        │       error_log_88.sdi
        │       events_errors_su_147.sdi
        │       events_errors_su_148.sdi
        │       events_errors_su_149.sdi
        │       events_errors_su_150.sdi
        │       events_errors_su_151.sdi
        │       events_stages_cu_119.sdi
        │       events_stages_hi_120.sdi
        │       events_stages_hi_121.sdi
        │       events_stages_su_122.sdi
        │       events_stages_su_123.sdi
        │       events_stages_su_124.sdi
        │       events_stages_su_125.sdi
        │       events_stages_su_126.sdi
        │       events_statement_127.sdi
        │       events_statement_128.sdi
        │       events_statement_129.sdi
        │       events_statement_130.sdi
        │       events_statement_131.sdi
        │       events_statement_132.sdi
        │       events_statement_133.sdi
        │       events_statement_134.sdi
        │       events_statement_135.sdi
        │       events_statement_136.sdi
        │       events_statement_137.sdi
        │       events_statement_138.sdi
        │       events_transacti_139.sdi
        │       events_transacti_140.sdi
        │       events_transacti_141.sdi
        │       events_transacti_142.sdi
        │       events_transacti_143.sdi
        │       events_transacti_144.sdi
        │       events_transacti_145.sdi
        │       events_transacti_146.sdi
        │       events_waits_cur_89.sdi
        │       events_waits_his_90.sdi
        │       events_waits_his_91.sdi
        │       events_waits_sum_92.sdi
        │       events_waits_sum_93.sdi
        │       events_waits_sum_94.sdi
        │       events_waits_sum_95.sdi
        │       events_waits_sum_96.sdi
        │       events_waits_sum_97.sdi
        │       file_instances_98.sdi
        │       file_summary_by__100.sdi
        │       file_summary_by__99.sdi
        │       global_status_190.sdi
        │       global_variables_193.sdi
        │       global_variable__197.sdi
        │       hosts_154.sdi
        │       host_cache_101.sdi
        │       keyring_componen_202.sdi
        │       keyring_keys_160.sdi
        │       log_status_183.sdi
        │       memory_summary_b_162.sdi
        │       memory_summary_b_163.sdi
        │       memory_summary_b_164.sdi
        │       memory_summary_b_165.sdi
        │       memory_summary_g_161.sdi
        │       metadata_locks_168.sdi
        │       mutex_instances_102.sdi
        │       objects_summary__103.sdi
        │       performance_time_104.sdi
        │       persisted_variab_198.sdi
        │       prepared_stateme_184.sdi
        │       processlist_105.sdi
        │       replication_appl_174.sdi
        │       replication_appl_175.sdi
        │       replication_appl_176.sdi
        │       replication_appl_177.sdi
        │       replication_appl_179.sdi
        │       replication_appl_180.sdi
        │       replication_asyn_181.sdi
        │       replication_asyn_182.sdi
        │       replication_conn_171.sdi
        │       replication_conn_173.sdi
        │       replication_grou_172.sdi
        │       replication_grou_178.sdi
        │       rwlock_instances_106.sdi
        │       session_account__159.sdi
        │       session_connect__158.sdi
        │       session_status_191.sdi
        │       session_variable_194.sdi
        │       setup_actors_107.sdi
        │       setup_consumers_108.sdi
        │       setup_instrument_109.sdi
        │       setup_loggers_110.sdi
        │       setup_meters_111.sdi
        │       setup_metrics_112.sdi
        │       setup_objects_113.sdi
        │       setup_threads_114.sdi
        │       socket_instances_155.sdi
        │       socket_summary_b_156.sdi
        │       socket_summary_b_157.sdi
        │       status_by_accoun_186.sdi
        │       status_by_host_187.sdi
        │       status_by_thread_188.sdi
        │       status_by_user_189.sdi
        │       table_handles_166.sdi
        │       table_io_waits_s_115.sdi
        │       table_io_waits_s_116.sdi
        │       table_lock_waits_117.sdi
        │       temporary_accoun_167.sdi
        │       threads_118.sdi
        │       tls_channel_stat_201.sdi
        │       users_152.sdi
        │       user_defined_fun_199.sdi
        │       user_variables_b_185.sdi
        │       variables_by_thr_192.sdi
        │       variables_info_195.sdi
        │       variables_metada_196.sdi
        │
        └───sys
                sys_config.ibd
